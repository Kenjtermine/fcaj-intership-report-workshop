---
title : "Demo tính năng giao dịch, ghi nhận lịch sử và tính chỉ số Carbon"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

## Demo tính năng giao dịch, ghi nhận lịch sử và tính chỉ số Carbon

Sau khi đã thực hiện việc seed dữ liệu số dư và thẻ cho demo, bạn sẽ hoàn thành việc demo tính năng giao dịch. Để thực hiện, bạn cần sử dụng nút **POS** đang được đặt tạm thời trên header của trang web, nút này sẽ mở ra một giao diện để mô phỏng vận hành của máy POS giả lập. Sau đó, bạn cần nhập vào mã MCC được seed bên dynamodb, nhập số tiền giao dịch, tên id máy pos và mô tả đơn hàng giả lập. Cuối cùng ấn vào **EXECUTE TRANSACTION** để hoàn thành giao dịch. 

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/1-pos-execute.png" width="80%" />

Sau khi giao dịch thành công, cửa số POS sẽ trả về message reponse có vai trò như thông tin biên lai. Tắt cửa số POS, reload trang web và bạn sẽ có kết quả trả về lịch sử giao dịch và số dư sau giao dịch và chỉ số Carbon được tính cộng thêm vào profile người dùng

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/2-pos-response.png" width="80%" />

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/3-profile-response.png" width="100%" />

Lúc này, bạn đã hoàn thành việc demo tính năng giao dịch, ghi nhận lịch sử và tính chỉ số Carbon và cũng như là bước cuối cùng của việc thực hành demo web, chúng tôi sẽ cố gắng phát triển và hoàn thiện các chức năng quan trọng khác để NaturEra Green Banking có thể trở thành một dự án ngân hàng số thực thụ có khả năng phát triển đưa vào ứng dụng thực tế doanh nghiệp. Chúng ta bước tới bước dọn dẹp để kết thúc workshop.
