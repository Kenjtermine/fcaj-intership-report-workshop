---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
<!-- {{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}} -->


### Week 4 Objectives:

* Create a project-based AWS SAM application using the design developed in Week 3.
* Set up DynamoDB (Single-Table Design) and Seed Data.
* Implement AWS Cognito to manage user authentication (Client/Staff).
* Develop `Transaction Lambda` core logic (transaction calculation logic).

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Create Infrastructure: Use AWS CLI/SAM CLI to create a project-based template.<br>&emsp; + Set up `template.yaml` for the GreenBankingTable (DynamoDB)                                        | 06/07/2026   | 06/07/2026      | <https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/> |
| 3   | - Authenticate & Authorize: Set up AWS Cognito User Pool for the staff and the client. <br>&emsp; + Update `template.yaml` to add Cognito                                                     | 07/07/2026   | 07/07/2026      | |
| 5   | - Core Logic: Write code for `Transaction Lambda`.<br>&emsp; + Interact with the CO2 calculation function in the `Transaction Lambda` using the Lambda Console.                               | 09/07/2026   | 10/07/2026      |                                           |
| 6   | - Data Setup (Mock Data): Write script to seed DynamoDB with mock data.<br>&emsp; + Fix 500 error when calling API.                                                          | 10/07/2026   | 10/07/2026      |                                           |
| 7   | - Testing & Review: Use `sam local invoke` to run the `Transaction Lambda` locally.<br>&emsp; + Review the code for the Lab 40.                                                                | 11/07/2026   | 11/07/2026      |                                           |


### Week 4 Achievements:

* Infrastructure as Code (IaC) using SAM has been successfully deployed.
* DynamoDB has been set up with a sample data table to allow the Frontend to call the API.
* Core function (`Transaction Lambda`) has been able to run locally and calculate the CO2 emissions.
* AWS Cognito has been set up with a user pool for the staff and the client.