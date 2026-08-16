---
title : "Clean up"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---
#### Clean Up Resources

Congratulations on successfully completing this lab! 

In this lab, you learned how to deploy a modern Serverless architecture for a digital banking project using Infrastructure as Code (IaC). You automated the creation of AWS Lambda, API Gateway, Amazon DynamoDB, and Amazon Cognito with just a few CLI commands.

To avoid unexpected charges (exceeding the Free Tier), it is crucial to clean up your infrastructure after you finish. Thanks to AWS SAM, this process is incredibly quick.

#### Cleanup Steps

1. **Delete all data in S3 frontend bucket**
   Open your Terminal in the directory containing your frontend code and run the following command:
   ```powershell
   aws s3 rm s3://<your-frontend-s3-bucket-name> --recursive
   ```
   Or simply go to **S3** on AWS Console and delete all data in frontend bucket. In **Buckets** folder, select your frontend bucket and choose **Empty** then **Delete**, enter bucket name and confirm to delete bucket.

   <img src="/fcaj-intership-report-workshop/images/5-Workshop/5.6-Cleanup/1-s3-empty-delete.png" width="80%" />

   <img src="/fcaj-intership-report-workshop/images/5-Workshop/5.6-Cleanup/2-s3-delete-confirm.png" width="80%" />

   After deleting all data in S3, you can delete the **Stack** using SAM CLI.

2. **Delete the entire Stack using SAM CLI**
   Open your Terminal in the directory containing your `template.yaml` file and run the following command to delete the entire stack:
   ```powershell
   sam delete
   ```
   The above command will delete all data and all resources in your stack within 10-15 minutes. This is the end of the workshop cleanup process.
   