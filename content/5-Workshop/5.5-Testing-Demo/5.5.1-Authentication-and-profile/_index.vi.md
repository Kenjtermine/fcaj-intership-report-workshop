---
title : "Xác thực tài khoản và tạo thông tin tài khoản"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---
## Xác thực tài khoản và tạo thông tin tài khoản

### Thực hiện đăng ký và xác nhận tài khoản
Khi vào trang web, bạn sẽ thấy giao diện đăng nhập tài khoản. Nếu bạn chưa có tài khoản, bạn có thể đăng ký một tài khoản mới bằng phần **Đăng ký**. Nhập email đăng kí, mật khẩu và xác nhận mật khẩu, sau đó ấn **Tạo tài khoản**.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/1-register.png" width="80%" />

Khi đăng kí thành công, trang web tự động điều hướng bạn sang trang xác nhận tài khoản bằng OTP gửi qua email đã đăng ký. Bạn có thể nhập OTP để xác nhận tài khoản.

{{% notice info %}}
Lưu ý: Nếu bạn không thấy mail otp của cognito, hãy thử mở mục **Spam** trong cửa sổ email của bạn. Dạng thư gửi đến thường là **no-reply@verificationemail.com**.
{{% /notice %}}

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/2-otp-confirm.png" width="80%" />

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/3-email-confirm.png" width="80%" />

Sau khi xác thực tài khoản bằng OTP thành công, bạn sẽ được điều hướng sang tab đăng nhập và có thể đăng nhập vào hệ thống.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/4-login.png" width="80%" />

### Thực hiện đăng nhập và tự động tạo thông tin tài khoản

Sau khi đăng nhập vào hệ thống, bạn sẽ thấy giao diện trang chủ của NaturEra Green Banking với hồ sơ thông tin được tự động tạo nếu chưa có, trên giao diện chính sẽ hiển thị tên tài khoản trùng với email đăng ký của bạn. Số dư ban đầu, chỉ số carbon đều ở số 0, lịch sử giao dịch trống, và chưa có thông tin thẻ.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/5-profile.png" width="80%" />

### Bước tiếp theo
Sau khi đăng nhập thành công và có hồ sơ, vì chưa có số dư ban đầu và thẻ, để thực hiện chức năng giao dịch, bạn cần phải nạp giả lập các dữ liệu về số dư và thẻ (seed data) ở bước sau.
[Seed các dữ liệu số dư và thẻ để demo tính năng](5.5.2-Seed-data-for-demo/)