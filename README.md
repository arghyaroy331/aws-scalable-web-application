# ☁️ AWS Scalable & Secure Blog Application

> A production-style, cloud-native blog application built on **AWS**, demonstrating real-world skills in compute, storage, networking, security, monitoring, and Infrastructure as Code (IaC).

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws&logoColor=white)
![Status](https://img.shields.io/badge/status-active-brightgreen)
![IaC](https://img.shields.io/badge/IaC-CloudFormation-blueviolet)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 📖 Table of Contents

- [🎯 Objective](#-objective)
- [💡 Problem Statement](#-problem-statement)
- [📌 System Architecture](#-system-architecture)
- [🔄 Application Workflow](#-application-workflow)
- [🔒 Security Features](#-security-features)
- [⚡ Scalability](#-scalability)
- [📊 AWS Services Explained](#-aws-services-explained)
- [🧠 Challenges Faced](#-challenges-faced)
- [📚 Key Learnings](#-key-learnings)
- [🎓 Suitable For](#-suitable-for)
- [🚀 Future Roadmap](#-future-roadmap)
- [👨‍💻 Author](#-author)

---

## 🎯 Objective

The primary objective of this project is to **design, deploy, and manage** a scalable, secure, and highly available blog application using **Amazon Web Services (AWS)**.

This project demonstrates practical cloud infrastructure deployment by integrating:

- 🖥️ Compute
- 💾 Storage
- 🌐 Networking
- 📈 Monitoring
- 📩 Messaging
- 🔐 Security
- ⚙️ Infrastructure as Code (IaC)

...into a single, cohesive solution.

**Core focus areas:**

| Focus Area | Description |
|---|---|
| ☁️ Cloud Infrastructure Deployment | End-to-end setup on AWS |
| 🔐 Secure Resource Configuration | IAM, VPC, encryption |
| 🌍 Scalable Web Hosting | EC2 + Load Balancer |
| ⚡ Serverless Event Processing | Lambda-driven automation |
| 🗄️ Database Integration | Amazon RDS (MySQL) |
| 🤖 Infrastructure Automation | CloudFormation (IaC) |
| 📊 Monitoring and Alerting | CloudWatch + SNS |
| ✅ AWS Best Practices | Security & scalability standards |

---

## 💡 Problem Statement

Traditional web applications hosted on a single server often face:

- ❌ Limited scalability
- ❌ Single point of failure
- ❌ Difficult infrastructure management
- ❌ Lack of automated deployment
- ❌ Weak monitoring and alerting
- ❌ Manual resource provisioning
- ❌ Poor storage management

✅ This project solves these issues by deploying the application using AWS cloud services with a **modular architecture** and **infrastructure automation**.

---

## 📌 System Architecture

The architecture consists of several AWS services working together across multiple layers:

### 👤 User Layer
- Users access the web application
- Requests are directed to the EC2-hosted web server

### 🖥️ Compute Layer
- **Amazon EC2** hosts the blog application
- **Amazon EBS** provides persistent storage

### 🌐 Networking Layer
- **Amazon VPC** isolates cloud resources
- **Public subnet** hosts the EC2 instance
- **Private subnet** is reserved for secure resources such as Amazon RDS
- **Security Groups** protect the infrastructure

### 💾 Storage Layer
- **Amazon S3** stores images and static assets
- 🔁 Versioning protects data from accidental deletion
- 🔒 Encryption secures stored objects

### 🗄️ Database Layer
- **Amazon RDS (MySQL)** stores application data
- Secure database communication occurs between EC2 and RDS

### ⚡ Serverless Layer
- **AWS Lambda** automatically processes uploaded images
- **Amazon SQS** handles asynchronous processing
- **Amazon SNS** sends notifications

### 📈 Monitoring Layer
**Amazon CloudWatch** monitors:
- 🔥 CPU Utilization
- ❤️ Resource Health
- 📊 Performance Metrics

🚨 CloudWatch alarms notify administrators whenever thresholds are exceeded.

---

## 🔄 Application Workflow

```
👤 User
   │
   ▼
🖥️ Amazon EC2
   │
   ▼
📝 Blog Application
   │
   ▼
🗄️ Amazon RDS (Store Posts)
   │
   ▼
🖼️ Amazon S3 (Store Images)
   │
   ▼
⚡ Lambda Trigger
   │
   ▼
📩 Amazon SQS
   │
   ▼
🔔 Amazon SNS
   │
   ▼
📈 CloudWatch Monitoring
   │
   ▼
🧑‍💼 Administrator
```

---

## 🔒 Security Features

This project implements multiple AWS security best practices:

### 🪪 Identity Management
- IAM User
- Least Privilege Principle
- MFA Enabled

### 🌐 Network Security
- Amazon VPC
- Security Groups
- Public & Private Subnets

### 🔐 Data Security
- AWS KMS Encryption
- S3 Encryption
- RDS Security

### 📊 Monitoring
- CloudWatch Metrics
- CloudWatch Alarms
- Infrastructure Monitoring

---

## ⚡ Scalability

### ✅ Current Implementation
- Application Load Balancer
- Amazon EC2
- Amazon S3
- Amazon RDS

### 🔮 Future Enhancements
- Auto Scaling Group
- CloudFront CDN
- Route 53
- AWS WAF
- Multi-AZ RDS

---

## 📊 AWS Services Explained

| Service | Role | Highlights |
|---|---|---|
| 🪪 **IAM** | Secure identity management | User Authentication, Role Management, Policy Management |
| 🖥️ **Amazon EC2** | Hosts the blog application | Web Hosting, Backend Processing, Application Execution |
| 💾 **Amazon EBS** | Persistent storage attached to EC2 | OS, Application Files, Log Storage |
| 🖼️ **Amazon S3** | Stores images, static assets & backups | Highly Durable, Scalable, Secure |
| 🗄️ **Amazon RDS** | Managed MySQL database | Blog Posts, User Data, Metadata |
| ⚡ **AWS Lambda** | Serverless event processing | No Server Management, Auto Scaling, Event Driven |
| 📩 **Amazon SQS** | Reliable message queuing | Decouples Services, Prevents Data Loss, Improves Reliability |
| 🔔 **Amazon SNS** | Notification services | Email Alerts, System Notifications |
| 📈 **Amazon CloudWatch** | Monitors AWS resources | CPU Usage, Memory, Logs, Alarms |
| ⚙️ **CloudFormation** | Automates infrastructure deployment | Repeatable Deployments, IaC, Version Control |

---

## 🧠 Challenges Faced

During development, several practical cloud deployment challenges were encountered:

- 🔧 Configuring IAM permissions securely
- 🔗 Connecting EC2 with Amazon RDS
- 🛡️ Managing Security Group rules
- 🖼️ Configuring S3 event triggers for Lambda
- 🚨 Setting up CloudWatch alarms
- 📄 Creating CloudFormation templates
- 🧩 Understanding service integrations
- 💰 Working within AWS Free Tier limitations

---

## 📚 Key Learnings

This project helped build hands-on experience in:

- 🪪 AWS Identity and Access Management
- 🌐 Virtual Private Cloud Networking
- 🖥️ EC2 Deployment
- 💾 Cloud Storage
- 🗄️ Database Management
- ⚡ Event-Driven Architecture
- 🧩 Serverless Computing
- ⚙️ Infrastructure Automation
- 🔒 Cloud Security
- 📈 Cloud Monitoring
- 💻 AWS CLI
- 📄 CloudFormation

---

## 🎓 Suitable For

This repository demonstrates practical experience relevant to roles such as:

- ☁️ AWS Cloud Engineer
- 🛠️ Cloud Support Associate
- 🔄 DevOps Engineer
- 🧯 Site Reliability Engineer (SRE)
- 🏗️ Infrastructure Engineer
- 🖥️ Cloud Administrator
- ⚙️ Cloud Operations Engineer

---

## 🚀 Future Roadmap

- 🌍 Route 53 Custom Domain
- 🚀 CloudFront CDN
- 🔒 HTTPS using ACM
- 📈 Auto Scaling Group
- 🛡️ AWS WAF
- 🐳 Docker Containerization
- ☸️ Kubernetes (Amazon EKS)
- 🔄 CI/CD using GitHub Actions
- 🏗️ Terraform Support
- ⚡ Amazon ElastiCache
- 🔑 AWS Secrets Manager
- 🌎 Multi-Region Deployment
- 🆘 Disaster Recovery Strategy

---

## 👨‍💻 Author

**Arghya Roy**
🎓 B.Tech in Information Technology
☁️ Cloud & DevOps Enthusiast

---

⭐ **If you found this project useful, consider giving it a star!**
