---
title : "Authenticate & create account profile"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---
## Authenticate & create account profile

### Register & confirm account
When you enter the web page, you will see the login account. If you do not have an account, you can create a new account by clicking on the **Register** button. Enter your email, password, and confirm password, then click on **Create Account**.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/1-register.png" width="80%" />

When you register successfully, the web page will automatically redirect to the confirmation page by sending an OTP to your email. You can enter the OTP to confirm your account.

{{% notice info %}}
Note: If you do not receive the email from cognito, please check your spam folder. The email format may be **no-reply@verificationemail.com**.
{{% /notice %}}

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/2-otp-confirm.png" width="80%" />

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/3-email-confirm.png" width="80%" />

After successfully confirming your account using the OTP, you will be redirected to the POS terminal page and you can log in to the system.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/4-login.png" width="80%" />

### Login and get profile 

After successfully logging in to the web, you will see the homepage of NaturEra Green Banking with the profile auto created if you have not created one before. The number of carbon credits is 0, the real-time carbon balance is 0, and the transactions are empty, and there is no card info in the dashboard.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.1-Authentication-and-profile/5-profile.png" width="80%" />

### Next step
Next, you will complete the seeding of carbon credits and carbon balances for demo.
[Seed carbon credits & carbon balances for demo](5.5.2-Seed-data-for-demo/)

