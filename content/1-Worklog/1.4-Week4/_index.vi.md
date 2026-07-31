
---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Khởi tạo dự án thực tế bằng AWS SAM dựa trên kiến trúc đã vẽ ở Tuần 3.
* Cấu hình cơ sở dữ liệu DynamoDB (Single-Table Design) và bơm dữ liệu mồi (Seed Data).
* Tích hợp AWS Cognito để quản lý xác thực người dùng (Client/Staff).
* Phát triển `Transaction Lambda` cốt lõi (tích hợp logic tính toán hệ số CO2).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Khởi tạo Infrastructure: Dùng AWS CLI/SAM CLI để tạo bộ khung dự án.<br>&emsp; + Thiết lập `template.yaml` cho bảng `GreenBankingTable` (DynamoDB)                                        | 06/07/2026   | 06/07/2026      | <https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/> |
| 3   | - Xác thực & Bảo mật: Cấu hình AWS Cognito User Pool cho khách hàng và nhân viên. <br>&emsp; + Cập nhật `template.yaml` để thêm Cognito                                                     | 07/07/2026   | 07/07/2026      |  |
| 5   | - Phát triển Core Logic: Bắt tay vào viết code cho `Transaction Lambda`. <br>&emsp; + Tích hợp công thức tính toán hệ số CO2 dựa trên số tiền/loại giao dịch.                               | 09/07/2026   | 10/07/2026      |                                           |
| 6   | - Dữ liệu giả lập (Mock Data): Viết script bơm dữ liệu Seed vào DynamoDB. <br>&emsp; + Xử lý lỗi 500 do thiếu dữ liệu khi gọi API.                                                          | 10/07/2026   | 10/07/2026      |                                           |
| 7   | - Testing & Review: Sử dụng `sam local invoke` để chạy thử và debug Lambda.<br>&emsp; + Họp nhóm review tiến độ code tuần 4.                                                                | 11/07/2026   | 11/07/2026      |                                           |

### Kết quả đạt được tuần 4:

* Bộ khung dự án Infrastructure as Code (IaC) bằng SAM đã sẵn sàng hoạt động.
* Cơ sở dữ liệu DynamoDB đã có dữ liệu mẫu để team Frontend có thể bắt đầu gọi API.
* Core function (`Transaction Lambda`) đã có thể chạy dưới local và tính toán được điểm CO2.
* Hệ thống phân quyền cơ bản với Cognito đã được thiết lập xong.