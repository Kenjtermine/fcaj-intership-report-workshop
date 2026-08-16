---
title : "Dọn dẹp tài nguyên"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

#### Dọn dẹp tài nguyên

Xin chúc mừng bạn đã hoàn thành xong bài thực hành này! 

Trong lab này, bạn đã học cách triển khai một kiến trúc Serverless hiện đại cho dự án ngân hàng số sử dụng Infrastructure as Code (IaC). Bạn đã tự động hóa việc tạo AWS Lambda, API Gateway, Amazon DynamoDB và Amazon Cognito chỉ bằng vài dòng lệnh.

Để tránh phát sinh chi phí ngoài ý muốn (vượt mức Free Tier), việc dọn dẹp hạ tầng sau khi hoàn thành là rất quan trọng. Nhờ sử dụng AWS SAM, quá trình này diễn ra vô cùng nhanh chóng.

#### Các bước dọn dẹp

1. **Xóa toàn bộ dữ liệu tĩnh của frontend trong S3**
   Mở Terminal tại thư mục chứa frontend của bạn và chạy lệnh sau:
   ```bash
   aws s3 rm s3://<tên-bucket-s3-frontend-của-bạn> --recursive
   ```
   Hoặc đơn giản hơn, bạn có thể trực tiếp vào **S3** trên AWS Console và xóa dữ liệu tĩnh của frontend. Vào mục **Buckets** và chọn **<tên-bucket-s3-frontend-của-bạn>** và chọn **Empty**  sau đó chọn **Delete**, tại ô confirm nhập tên bucket và xác nhận xóa **Delete bucket**.

   <img src="/fcaj-intership-report-workshop/images/5-Workshop/5.6-Cleanup/1-s3-empty-delete.png" width="80%" />

   <img src="/fcaj-intership-report-workshop/images/5-Workshop/5.6-Cleanup/2-s3-delete-confirm.png" width="80%" />

   Sau khi xóa hết dữ liệu S3, bạn mới có thể xóa **Stack** bằng SAM CLI.

2. **Xóa toàn bộ Stack bằng SAM CLI**
   Mở Terminal tại thư mục chứa file `template.yaml` của bạn và chạy lệnh sau:
   ```powershell
   sam delete
   ```
   Thao tác trên sẽ xóa toàn bộ dữ liệu và tất cả các tài nguyên của bạn trong stack với thời gian chờ đầu tiên là khoảng từ 10-15 phút. Bước này kết thúc quá trình dọn dẹp workshop.