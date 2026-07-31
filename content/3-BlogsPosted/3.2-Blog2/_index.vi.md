# Kiến trúc Event-Driven: Cách Pelago cho AI "thời gian suy nghĩ" mà vẫn phản hồi coach dưới 100ms
Chào mọi người trong group,
Tuần này mình đọc được một case-study khá hay trên AWS Architecture Blog, kể về cách đội kỹ thuật của Pelago — một công ty y tế số chuyên hỗ trợ điều trị rối loạn sử dụng chất kích thích — xây dựng một trợ lý AI cho đội coach chỉ trong 2 tuần, hoàn toàn bằng serverless. Mình xin tóm tắt và chia sẻ vài điều rút ra được, vì thấy áp dụng được cho các dự án serverless khác của nhóm (kể cả project tụi mình đang làm).
### Bài toán đặt ra
Mỗi coach của Pelago theo dõi hàng chục cuộc hội thoại cùng lúc, mỗi cuộc kéo dài hàng tuần/tháng. Để phản hồi phù hợp, coach cần nắm toàn bộ lịch sử trò chuyện — rất tốn thời gian nếu soạn thủ công. Nhưng vì là ngành y tế nên có 3 ràng buộc khó nhằn: AI chỉ được gợi ý, con người vẫn phải duyệt trước khi gửi; dữ liệu bệnh nhân (PHI) tuyệt đối không được đi qua internet công cộng; và coach cần thấy gợi ý ngay khi mở hội thoại, trong khi xử lý hàng trăm tin nhắn qua LLM vốn tốn vài giây tới vài chục giây.
Giải pháp: tách "sinh gợi ý" ra khỏi "hiển thị gợi ý"
Thay vì gọi AI ngay lúc coach mở app (sẽ rất chậm), nhóm Pelago xử lý bất đồng bộ. Mỗi khi có tin nhắn mới, hệ thống publish một sự kiện lên Amazon SNS. SNS lập tức fan-out sự kiện này tới nhiều Lambda function độc lập cùng lúc: một hàm lưu metadata, một hàm gửi dữ liệu phân tích, một hàm gửi push notification, và một hàm "Chat Assistant" chuyên sinh gợi ý AI.
Hàm Chat Assistant chạy nền, không chặn luồng chính: nó lấy toàn bộ lịch sử hội thoại từ DynamoDB (đọc dưới 20ms dù hội thoại có 50+ tin nhắn), format lại thành ngữ cảnh, rồi gọi Amazon Bedrock (model Claude) để sinh gợi ý và lưu kết quả vào MySQL trên RDS. Toàn bộ quá trình này mất chưa tới 4 giây. Khi coach thật sự mở hội thoại (có thể vài phút hoặc vài giờ sau), app chỉ cần query MySQL lấy gợi ý đã có sẵn — nên thời gian phản hồi cảm nhận được chưa tới 100ms.
Điểm mình thấy hay nhất: nhờ tách "sinh" và "đọc" thành hai luồng riêng qua SNS, muốn thêm tính năng mới (như AI Assistant này) chỉ cần đăng ký thêm một Lambda subscriber, không cần đụng vào code cũ đang chạy production.
### Vài quyết định implementation đáng chú ý
Bảo mật dữ liệu y tế: dùng VPC Endpoint cho Bedrock để traffic gọi model không ra internet công cộng, mã hoá dữ liệu at-rest, IAM least-privilege, log CloudWatch chỉ ghi message ID chứ không ghi nội dung.
Polyglot đúng bài toán: Lambda gọi Bedrock viết bằng Python (Boto3 hỗ trợ Bedrock tốt), Lambda truy xuất dữ liệu viết bằng TypeScript để đồng bộ backend còn lại — chọn ngôn ngữ theo use-case chứ không ép một runtime cho cả hệ thống.
Idempotency: vì SNS có thể deliver trùng, Lambda luôn kiểm tra MySQL xem gợi ý đã tồn tại chưa trước khi gọi Bedrock lần nữa, tránh tốn tiền và tránh sinh 2 gợi ý mâu thuẫn.
Chi phí theo traffic thực tế: traffic tập trung giờ hành chính, mô hình pay-per-invocation của Lambda giúp hệ thống tự scale theo giờ cao điểm mà không tốn chi phí idle — kể cả khi traffic tăng đột biến 8 lần, hệ thống vẫn chạy ổn không cần chỉnh cấu hình.
### Kết quả
Nhóm Pelago đi từ ý tưởng tới production chỉ trong 2 tuần. Sau triển khai, thời gian chuẩn bị phản hồi của coach giảm trung bình 40%, và khoảng 79.6% gợi ý AI được coach đánh giá là hữu ích.
Những gì mình rút ra được
Xử lý bất đồng bộ (pre-compute rồi cache kết quả) là cách kinh điển để cho AI "thời gian suy nghĩ" mà vẫn giữ trải nghiệm người dùng nhanh.
SNS fan-out là pattern mạnh để thêm tính năng mới mà không sợ phá hệ thống cũ.
Chọn DynamoDB hay RDS nên theo access pattern (ghi nhanh/đọc theo key → DynamoDB; cần query linh hoạt/join → RDS), không theo thói quen.
Idempotency check là bắt buộc khi dùng messaging bất đồng bộ, vì at-least-once delivery luôn có khả năng gửi trùng.
Cảm ơn mọi người đã đọc, mong nhận thêm góp ý về cách áp dụng pattern event-driven này cho các bài toán serverless khác!
Nguồn: AWS Architecture Blog — "Building a serverless AI assistant at Pelago: concept to care in two weeks"
https://aws.amazon.com/blogs/architecture/building-a-serverless-ai-assistant-at-pelago-concept-to-care-in-two-weeks/