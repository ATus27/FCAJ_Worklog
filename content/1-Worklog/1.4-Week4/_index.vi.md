---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Tìm hiểu chuyên sâu các dịch vụ AWS Lambda, S3 Event Notification, SQS (Standard, DLQ, retry policy) và Amazon Textract (OCR).
* Cấu hình phân quyền theo nguyên tắc tối thiểu (least privilege) và resource-based policy giữa các dịch vụ.
* Hoàn thiện Luồng 1 (Data Ingestion Pipeline): S3 (upload), S3 Event SQS (buffer), Lambda (Document Processor), Textract OCR.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu chuyên sâu kiến trúc AWS Lambda, S3 Event Notification, SQS (Standard Queue, DLQ, retry policy) và Amazon Textract (OCR). | 13/07/2026 | 13/07/2026 | AWS Documentation |
| 3 | - Nghiên cứu và cấu hình phân quyền nguyên tắc tối thiểu (least privilege) và resource-based policy giao tiếp an toàn giữa S3, SQS, Lambda và Textract. | 14/07/2026 | 14/07/2026 | AWS IAM & Security Guide |
| 4 | - Khởi tạo S3 Bucket tiếp nhận tài liệu tải lên (PDF/Image scan) và cấu hình SQS Queue làm buffer tin nhắn kèm Dead Letter Queue (DLQ) nâng cao độ tin cậy. | 15/07/2026 | 15/07/2026 | AWS SQS & S3 Event Guide |
| 5 | - Phát triển AWS Lambda (Document Processor) kết nối SQS Event Source Mapping và gọi Amazon Textract API thực hiện bóc tách văn bản (OCR). | 16/07/2026 | 16/07/2026 | Amazon Textract Developer Guide |
| 6 | - Kiểm thử hoàn thiện Luồng 1 end-to-end: Upload tài liệu mẫu lên S3 ➔ SQS buffer ➔ Lambda Document Processor ➔ Textract OCR; kiểm tra CloudWatch Logs. | 17/07/2026 | 17/07/2026 | Internal Test Suite |

### Kết quả đạt được tuần 4:

* **Làm chủ kiến thức Serverless & OCR**: Hiểu rõ nguyên lý hoạt động của S3 Event Notifications, cơ chế buffer và retry của SQS Standard/DLQ, cùng quy trình trích xuất văn bản tự động qua Amazon Textract API.
* **Chuẩn hóa phân quyền IAM**: Thiết lập thành công IAM Roles & Resource-based Policies tuân thủ nguyên tắc tối thiểu (least privilege), đảm bảo bảo mật tuyệt đối cho giao tiếp giữa các dịch vụ.
* **Hoàn thiện Luồng 1 (Data Ingestion)**: Xây dựng thành công pipeline tiếp nhận tài liệu tự động từ S3 qua SQS buffer, kích hoạt Lambda xử lý OCR với Textract và sẵn sàng cho các công đoạn vector hóa tiếp theo.
