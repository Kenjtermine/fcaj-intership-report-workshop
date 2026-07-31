---
title: "Event 1: AWS Enterprise Cloud Architectures & Industry Application"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

## Event Objectives: 
* Exploring solutions and architectures for building a serverless application
* Understanding the core components of serverless architecture
* Analyzing many real-world industrial applications in the financial services industry, including the challenges of security and compliance, and the best practices for landing zones to protect data.

### Featured Topics & Solutions
* **Cloud Kinetics - FinOps: Modernizing FinOps with Cloud Migration & FinOps:** This talk will cover the latest architecture for migrating large systems. Take a deep dive into FinOps and how it can help manage AWS costs, monitor Cloud - a perfect fit when building a financial services system that needs Audit logs.
* **Renova Cloud - Modernizing Applications & Data (App Modernization & Data):** Share the way to architect applications in a monolith (Monolith) to Microservices (Microservices) using Serverless and EKS. AI/ML and Data Lake into data analysis and warehousing.
* **Industry Applications (Industry Applications):** Analyze the security and compliance challenges and best practices for the Financial Services Industry. Set up Landing Zones to protect data.

### Event Experience
The experience of exploring solutions and architectures for building a serverless application and understanding the core components of serverless architecture is similar to the experience of building a Lab in a team without a build Lab.
* **Enterprise thinking (Enterprise architecture):** It is clear that in a large system, the architecture should not be just functional, but should address security and compliance challenges at multiple layers, use high availability (Multi-AZ) and disaster recovery (Disaster Recovery).
* **Connecting FCAJ internals to the cloud:** Some considerations on security and compliance and how FCAJ internal data is handled in a way that is compatible with our architecture for Identity (Cognito) and IAM (Security Isolation) for the TransactionEngine vs. ReportGenerator Lambda functions in the Digital Banking application.
 ### Lessons Learned
* **Cloud architecture should balance cost and functionality:** Every decision to choose a technology (e.g., use Aurora Serverless or DynamoDB, use EC2 or Fargate) should be made to meet the SLA (Service Level Agreement) and cost goals.
* **FinOps is ongoing:** It is not the end of the cloud. Monitoring, tagging (e.g., using AWS Resource Groups instead of myApplications) to track cost is a key enabler of a Cloud Architect.
* **Time-to-market is a function of the project:** For large projects, the time to market (TTM) is a function of the size of the project, not the Cloud Architect.