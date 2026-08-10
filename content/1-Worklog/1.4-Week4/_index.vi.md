---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Chuẩn bị môi trường phát triển, cấu hình công cụ AWS CLI & Terraform IaC.
* Đăng ký quyền truy cập model trên Amazon Bedrock (Claude 3 & Titan Embeddings).
* Triển khai hạ tầng khối Ingestion đầu tiên: S3 Bucket, SQS Queue kèm DLQ và AWS Lambda xử lý OCR với Amazon Textract (Luồng 1 - Data Ingestion).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Cấu hình tài khoản AWS tại Region **N. Virginia (us-east-1)**.<br>- Gửi yêu cầu xin quyền truy cập (Model Access) các model trên **Amazon Bedrock**: *Claude 3 (Haiku & Sonnet)* và *Amazon Titan Embeddings*.<br>- Cài đặt các công cụ phát triển: AWS CLI v2, Terraform (>=1.5), Python 3.12, Git, VS Code. | 13/07/2026 | 13/07/2026 | Workshop Section 5.2 |
| 3 | - Thiết lập IAM User & IAM Policies cấp quyền đủ cho Terraform (Compute, S3, SQS, DynamoDB, OpenSearch, Bedrock, Cognito, CloudWatch).<br>- Khởi tạo tài khoản **HCP Terraform** (app.terraform.io) để quản lý remote state.<br>- Khởi tạo thư mục dự án Terraform (`main.tf`, `variables.tf`, `outputs.tf`, `providers.tf`). | 14/07/2026 | 14/07/2026 | Workshop Section 5.2.1 - 5.2.3 |
| 4 | - **Luồng 1 - Triển khai S3 Bucket**: Viết module Terraform tạo Amazon S3 Bucket lưu trữ tài liệu gốc (PDF, TXT, PNG/JPG scan).<br>- Cấu hình S3 Lifecycle rule, Encryption (SSE-S3), Block Public Access.<br>- Tạo **Amazon SQS Queue** kèm **Dead Letter Queue (DLQ)** để hứng thông báo S3 Event. | 15/07/2026 | 15/07/2026 | Workshop Section 5.3 |
| 5 | - Cấu hình S3 Event Notification tự động đẩy tin nhắn vào SQS khi có file mới được tải lên.<br>- Khởi tạo **AWS Lambda** (Document Processing Lambda) kết nối SQS làm Event Source Mapping.<br>- Viết code Python bóc tách nội dung file bằng **Amazon Textract** (`DetectDocumentText` / `AnalyzeDocument`). | 16/07/2026 | 16/07/2026 | Workshop Section 5.3 |
| 6 | - **Thử nghiệm độc lập**: Upload file PDF/scan mẫu lên S3 Bucket.<br>- Kiểm tra luồng: S3 ➔ SQS ➔ Lambda Textract.<br>- Kiểm tra Log đầu ra của Textract trong AWS CloudWatch Logs. | 17/07/2026 | 17/07/2026 | Workshop Section 5.3 & 5.10 |

### Kết quả đạt được tuần 4:

* **Chuẩn bị môi trường & IaC**: Cài đặt thành công bộ công cụ phát triển (AWS CLI v2, Terraform, Python 3.12). Đã kích hoạt quyền truy cập Amazon Bedrock Models (Claude 3 & Titan Embeddings).
* **Quản lý hạ tầng bằng Terraform**: Thiết lập thành công HCP Terraform Remote State và tạo cấu trúc module IaC dự án.
* **Xây dựng khối Ingestion nền tảng**: Tự động hóa luồng nhận sự kiện upload tài liệu từ S3 Bucket qua SQS Queue và trigger Lambda bóc tách văn bản OCR thành công bằng Amazon Textract.
