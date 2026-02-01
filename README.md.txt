# 📦 AWS S3 File Upload Logger (Lambda + Python)

![AWS](https://img.shields.io/badge/AWS-Lambda-orange)
![Python](https://img.shields.io/badge/Python-3.11-blue)
![Serverless](https://img.shields.io/badge/Serverless-Yes-success)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 🚀 Project Overview

This project demonstrates an **event-driven serverless architecture** using AWS.  
Whenever a file is uploaded to an S3 bucket, an AWS Lambda function (Python) is automatically triggered to log file metadata such as:

- Bucket name  
- File name  
- File size  

The logs are stored and verified using **Amazon CloudWatch**.

---

User → Upload File → Amazon S3
↓
Event Notification
↓
AWS Lambda (Python)
↓
CloudWatch Logs


---

## 🛠️ Technologies Used

- AWS S3
- AWS Lambda (Python 3.11)
- AWS IAM
- Amazon CloudWatch
- Git & GitHub

---

## ⚙️ Lambda Function Logic

```python
bucket_name = record['s3']['bucket']['name']
file_name = record['s3']['object']['key']
file_size = record['s3']['object']['size']


The Lambda function extracts metadata from the S3 event and logs it.

New file uploaded to S3
Bucket Name: lambda-s3-demo-irfan
File Name: AI+Automation-in-excel.pdf
File Size: 192753 bytes

🔐 IAM Permissions Used

AmazonS3ReadOnlyAccess

CloudWatchLogsFullAccess

📌 Key Learnings

Event-driven serverless architecture

S3 → Lambda triggers

IAM role-based access

CloudWatch monitoring & debugging

Real-time validation using file metadata

🧑‍💻 Author

Irfan Pasha
Cloud & DevOps Enthusiast
📍 Bangalore, India

## 🧠 Architecture Flow

