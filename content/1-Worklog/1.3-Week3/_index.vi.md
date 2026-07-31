---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
<!-- {{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}} -->


### Mục tiêu tuần 3:

* Họp lần 2 để lên ý tưởng chốt tổng hợp của dự án.
* Tìm hiểu, xem các bài viết về ý tưởng mới ngân hàng xanh của dự án vừa chốt.
* Sửa lại bản thiết kế của dự án theo ý tưởng mới ngân hàng.
* Tìm hiểu thêm các dịch vụ khác phục vụ cho Serverless application.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Lên lịch meeting với các thành viên để cùng nhau suy nghĩ ý tưởng mới cho dự án ngân hàng: <br>&emsp; + Nhóm thành viên quyết định mô hình Green Banking cho dự án                                                                                           | 29/06/2026   | 29/06/2026      |
| 3   | - Tìm các bài viết, nguồn tài liệu liên quan tới mô hình Green Banking                                             | 30/06/2026   | 1/07/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Thiết kế hệ thống dự án dựa trên các sơ đồ mẫu kiến trúc serverless: <br>&emsp; + Tạo Cloudformation template cho các dịch vụ AWS <br>&emsp; + Tạo Lambda function  <br>&emsp; + ...                                                                                           | 2/07/2026    | 3/07/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Thực hiện lab 80: <br>&emsp; + Triển khai frontend có sẵn <br>&emsp; + Tạo Lambda function để xử lý kích thước ảnh kết nối S3 <br>&emsp; + Tạo Lambda function để ghi dữ liệu vào DynamoDB <br>&emsp; + ... | 3/07/2026    | 3/07/2026      | <https://000080.awsstudygroup.com/> |
| 7   | - Tham gia event online - event AWS Enterprise Cloud Architectures & Industry Application                                                                                                                                                                                                                                                                                                                                                                              | 4/07/2026    | 4/07/2026      |


### Kết quả đạt được tuần 3:

* Ý tưởng mới của nhóm chốt là mô hình Green Banking trong dự án ngân hàng
* Tìm hiểu về bài viết và các tài liệu để hiểu được mô hình hoạt động thế nào, ý nghĩa và sứ mệnh của nó. Tiếp tục tìm hiểu thêm để rõ hơn trong tuần tới
* Vẽ lại kiên trúc: Thiết kế các core lambda function kết nối bằng API Gateway, core lambda là Transaction Lambda - thực hiện giao dịch
* Thực hiện lab để hiểu rõ về SAM - Serverless Application Model, giúp cho lập trình viên nhanh chóng xây dựng và triển khai các dịch vụ AWS




