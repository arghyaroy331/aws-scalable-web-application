# AWS Scalable Web Application Deployment

This project demonstrates deployment of a scalable blog/web application using Amazon Web Services (AWS).

Services Used

- IAM – Identity and Access Management
- VPC – Network isolation
- EC2 – Web server hosting
- Application Load Balancer – Traffic distribution
- Amazon S3 – Static file storage
- Amazon RDS – MySQL database
- SNS – Notification service
- SQS – Message queue
- AWS Lambda – Serverless image processing
- CloudWatch – Monitoring and alarms
- CloudFormation – Infrastructure automation

## Architecture
![AWS Architecture](architecture-diagram.png)

The architecture uses EC2 instances behind an Application Load Balancer inside a VPC. Static files are stored in S3 and the database is hosted on Amazon RDS. Serverless processing is implemented with Lambda, SNS, and SQS.

Monitoring and Automation

CloudWatch alarms monitor CPU utilization and system metrics. Infrastructure resources are automated using CloudFormation templates deployed through AWS CLI.
