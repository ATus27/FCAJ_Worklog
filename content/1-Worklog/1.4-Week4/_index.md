---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:

* In-depth research on AWS Lambda, S3 Event Notification, SQS (Standard, DLQ, retry policy), and Amazon Textract (OCR).
* Configure least privilege access and resource-based policies between AWS services.
* Finalize Stream 1 (Data Ingestion Pipeline): S3 (upload), S3 Event SQS (buffer), Lambda (Document Processor), Textract OCR.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Deep dive into AWS Lambda architecture, S3 Event Notification, SQS (Standard Queue, DLQ, retry policy), and Amazon Textract (OCR). | 07/13/2026 | 07/13/2026 | AWS Documentation |
| Tue | - Research and configure least privilege IAM permissions and resource-based policies for secure communication between S3, SQS, Lambda, and Textract. | 07/14/2026 | 07/14/2026 | AWS IAM & Security Guide |
| Wed | - Set up S3 Bucket for document uploads (PDF/scanned images) and SQS Queue with Dead Letter Queue (DLQ) as a resilient message buffer. | 07/15/2026 | 07/15/2026 | AWS SQS & S3 Event Guide |
| Thu | - Develop AWS Lambda (Document Processor) connected via SQS Event Source Mapping to invoke Amazon Textract API for OCR text extraction. | 07/16/2026 | 07/16/2026 | Amazon Textract Developer Guide |
| Fri | - Test and finalize Stream 1 end-to-end: Document upload to S3 ➔ SQS buffer ➔ Lambda Document Processor ➔ Textract OCR; verify CloudWatch Logs. | 07/17/2026 | 07/17/2026 | Internal Test Suite |

### Week 4 Achievements:

* **Mastered Serverless & OCR Fundamentals**: Gained deep knowledge of S3 Event Notifications, SQS Standard/DLQ retry mechanisms, and automated text extraction via Amazon Textract API.
* **Standardized IAM Security**: Configured least-privilege IAM Roles and Resource-based Policies ensuring secure inter-service communications.
* **Finalized Stream 1 (Data Ingestion)**: Built a fully functional document ingestion pipeline from S3 to SQS buffer and Lambda Textract OCR execution.
