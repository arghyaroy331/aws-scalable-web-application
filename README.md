The primary objective of this project is to design, deploy, and manage a scalable, secure, and highly available blog application using Amazon Web Services (AWS). The project demonstrates practical cloud infrastructure deployment by integrating compute, storage, networking, monitoring, messaging, security, and Infrastructure as Code (IaC) services into a single solution.

The implementation focuses on:

Cloud Infrastructure Deployment
Secure Resource Configuration
Scalable Web Hosting
Serverless Event Processing
Database Integration
Infrastructure Automation
Monitoring and Alerting
AWS Best Practices
💡 Problem Statement

Traditional web applications hosted on a single server often face challenges such as:

Limited scalability
Single point of failure
Difficult infrastructure management
Lack of automated deployment
Weak monitoring and alerting
Manual resource provisioning
Poor storage management

This project solves these issues by deploying the application using AWS cloud services with modular architecture and infrastructure automation.

📌 System Architecture

The architecture consists of several AWS services working together.

User Layer
Users access the web application.
Requests are directed to the EC2-hosted web server.
Compute Layer
Amazon EC2 hosts the blog application.
Amazon EBS provides persistent storage.
Networking Layer
Amazon VPC isolates cloud resources.
Public subnet hosts the EC2 instance.
Private subnet is reserved for secure resources such as Amazon RDS.
Security Groups protect the infrastructure.
Storage Layer
Amazon S3 stores images and static assets.
Versioning protects data from accidental deletion.
Encryption secures stored objects.
Database Layer
Amazon RDS MySQL stores application data.
Database communication occurs between EC2 and RDS.
Serverless Layer

AWS Lambda automatically processes uploaded images.

Amazon SQS handles asynchronous processing.

Amazon SNS sends notifications.

Monitoring Layer

Amazon CloudWatch monitors:

CPU Utilization
Resource Health
Performance Metrics

CloudWatch alarms notify administrators whenever thresholds are exceeded.

🔄 Application Workflow
User

↓

Amazon EC2

↓

Blog Application

↓

Amazon RDS (Store Posts)

↓

Amazon S3 (Store Images)

↓

Lambda Trigger

↓

Amazon SQS

↓

Amazon SNS

↓

CloudWatch Monitoring

↓

Administrator
🔒 Security Features

This project implements multiple AWS security best practices.

Identity Management
IAM User
Least Privilege Principle
MFA Enabled
Network Security
Amazon VPC
Security Groups
Public & Private Subnets
Data Security
AWS KMS Encryption
S3 Encryption
RDS Security
Monitoring
CloudWatch Metrics
CloudWatch Alarms
Infrastructure Monitoring
⚡ Scalability

The project is designed with scalability in mind.

Current Implementation

Application Load Balancer
Amazon EC2
Amazon S3
Amazon RDS

Future Enhancements

Auto Scaling Group
CloudFront CDN
Route 53
AWS WAF
Multi-AZ RDS
📊 AWS Services Explanation
IAM

Provides secure identity management.

Used for:

User Authentication
Role Management
Policy Management
Amazon EC2

Hosts the blog application.

Responsibilities:

Web Hosting
Backend Processing
Application Execution
Amazon EBS

Persistent storage attached to EC2.

Used for:

Operating System
Application Files
Log Storage
Amazon S3

Stores:

Images
Static Assets
Backup Files

Benefits:

Highly Durable
Scalable
Secure
Amazon RDS

Managed MySQL database.

Stores:

Blog Posts
User Data
Metadata
Lambda

Executes serverless functions whenever new images are uploaded to S3.

Benefits:

No Server Management
Automatic Scaling
Event Driven
Amazon SQS

Provides reliable message queuing.

Benefits:

Decouples Services
Prevents Data Loss
Improves Reliability
Amazon SNS

Provides notification services.

Uses:

Email Alerts
System Notifications
CloudWatch

Monitors AWS resources.

Tracks:

CPU Usage
Memory
Logs
Alarms
CloudFormation

Automates AWS infrastructure deployment.

Benefits:

Repeatable Deployments
Infrastructure as Code
Version Control
🧠 Challenges Faced

During the development of this project, several practical cloud deployment challenges were encountered:

Configuring IAM permissions securely
Connecting EC2 with Amazon RDS
Managing Security Group rules
Configuring S3 event triggers for Lambda
Setting up CloudWatch alarms
Creating CloudFormation templates
Understanding service integrations
Working within AWS Free Tier limitations
📚 Key Learnings

This project helped me gain practical experience in:

AWS Identity and Access Management
Virtual Private Cloud Networking
EC2 Deployment
Cloud Storage
Database Management
Event-Driven Architecture
Serverless Computing
Infrastructure Automation
Cloud Security
Cloud Monitoring
AWS CLI
CloudFormation
🎓 Suitable For

This repository demonstrates practical experience relevant to roles such as:

AWS Cloud Engineer
Cloud Support Associate
DevOps Engineer
Site Reliability Engineer (SRE)
Infrastructure Engineer
Cloud Administrator
Cloud Operations Engineer
🚀 Future Roadmap

Planned improvements include:

Route 53 Custom Domain
CloudFront CDN
HTTPS using ACM
Auto Scaling Group
AWS WAF
Docker Containerization
Kubernetes (Amazon EKS)
CI/CD using GitHub Actions
Terraform Support
Amazon ElastiCache
AWS Secrets Manager
Multi-Region Deployment
Disaster Recovery Strategy


👨‍💻 Author
Arghya Roy
B.Tech in Information Technology
Cloud & DevOps Enthusiast
