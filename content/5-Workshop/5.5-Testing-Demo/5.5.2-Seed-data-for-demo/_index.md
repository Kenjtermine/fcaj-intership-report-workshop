---
title : "Seed carbon credits & carbon balances for demo"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.5.2. </b> "
---

## Seed carbon credits & carbon balances for demo

### Setup environment variables and execute the seed command

To complete the transaction feature, you need to seed the data for the carbon credits and carbon balances (seed data) in the next step. Login to AWS Console with your account and navigate to **Cognito** > **Users** > **User Pools** > **NaturEraGreenBankingUserPool** and copy the **USER ID** of the account you want to seed.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/1-cognito.png" width="80%" />

Back in the IDE, navigate to the directory containing your `template.yaml` file and run the following command:
```powershell
%project-root%\fcj-workshop-bui-quang-anh-kiet\backend\
$env:TABLE_NAME="NaturEraGreenBankingTable" || <table name>
$env:AWS_REGION=<AWS region>
$env:USER_ID=<USER ID>
$env:BALANCE=<Carbon balance to seed>
npm run seed
```
After running the command, you will receive the results of the seeded data (to ensure, you need to ensure the DynamoDB table name and environment variables are set). The result should look like this:

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/2-seed.png" width="80%" />

### Check the seeded data

To ensure, you need to reload the web, check the carbon balance and carbon credits have been updated. Then, you can go to the AWS Console DynamoDB, select the **NaturEraGreenBankingTable** (or the table name you set) in the **Tables** folder and select **Explore table items**. Here you can see the seeded data has been successfully updated or not.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/3-web-check.png" width="80%" />
<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.2-Seed-data-for-demo/4-dynamodb-check.png" width="80%" />

### Next step
After the data has been successfully seeded in both the web interface and DynamoDB, the next step is to complete the transaction feature demo. 

[Demo transaction feature, record receipts & calculate CO₂](5.5.3-Demo-transaction-feature/)