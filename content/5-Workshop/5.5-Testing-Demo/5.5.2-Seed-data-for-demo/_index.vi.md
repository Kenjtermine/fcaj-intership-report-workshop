---
title : "Seed các dữ liệu số dư và thẻ để demo tính năng"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.5.2. </b> "
---

## Seed các dữ liệu số dư và thẻ để demo tính năng

### Setup các biến môi trường và thực hiện lệnh seed

Để thực hiện chức năng giao dịch, bạn cần phải nạp giả lập các dữ liệu về số dư và thẻ (seed data) ở bước sau. Đăng nhập AWS Console bằng tài khoản dùng để configure sam backend ở bước trước. Vào phần **Cognito**, chọn **Users** ở phần **User Management** trong thanh sidebar. Copy mã User ID (Sub) của tài khoản bạn muốn dùng để seed data.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/1-cognito.png" width="80%" />

Quay lại trong IDE, tại terminal chạy backend, sử dụng mã User ID bạn đã copy và tên bảng DynamoDB để thiết lập biến môi trường:
```powershell
%project-root%\fcj-workshop-bui-quang-anh-kiet\backend\
$env:TABLE_NAME="NaturEraGreenBankingTable" || <tên bảng DynamoDB khác>
$env:AWS_REGION=<AWS region của bạn>
$env:USER_ID=<mã User ID của bạn>
$env:BALANCE=<Số dư bạn muốn thiết lập>
npm run seed
```
Sau khi chạy lệnh, bạn nhận được kết quả các dữ liệu được seed như sau (để đảm bảo, bạn cần phải đảm bảo tên bảng DynamoDB và biến môi trường đã được thiết lập ở trên). Kết quả mong đợi như sau:
<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/2-seed.png" width="80%" />

### Kiểm tra lại dữ liệu trên web và trong bảng dữ liệu ở DynamoDB
Để đảm bảo, bạn cần reload lại web, xem số dư và thẻ đã được seed ở bước trước được cập nhật thành công. Sau đó, bạn có thể vào DynamoDB của AWS Console, chọn bảng dữ liệu **NaturEraGreenBankingTable** (hoặc tên bảng của bạn đặt) tại mục **Tables** và chọn **Explore table items**. Tại đây bạn có thể xem các dữ liệu được seed thành công hay chưa.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/3-web-check.png" width="80%" />
<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/4-dynamodb-check.png" width="80%" />

### Bước tiếp theo
Sau khi dữ liệu đã được seed thành công thấy ở cả giao diện web và DynamoDB,bước seeding các dữ liệu chính thức thành công, tiếp theo là bước demo tính năng giao dịch (transaction) của NaturEra Green Banking.

[Demo tính năng giao dịch, ghi nhận lịch sử và tính chỉ số Carbon](5.5.3-Demo-transaction-feature/)
