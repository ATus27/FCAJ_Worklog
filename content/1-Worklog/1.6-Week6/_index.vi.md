---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Triển khai Luồng 3 (Monitoring & Alerting): CloudWatch Custom Metrics, CloudWatch Dashboards, Alarms, SNS Topics và AWS Chatbot tích hợp Slack.
* Triển khai Luồng 4 (RAGAS Evaluation): Nghiên cứu framework RAGAS, lập lịch EventBridge Scheduler và xây dựng Lambda Evaluation Runner tự động đánh giá chất lượng RAG.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **CloudWatch Advanced & Custom Metrics**: Đẩy custom metrics từ Lambda bằng `put_metric_data` (`boto3`); dựng CloudWatch Dashboard tổng quan (Lambda invocation/error rate, API Gateway 4xx/5xx, SQS queue depth). | 27/07/2026 | 27/07/2026 | AWS CloudWatch Documentation |
| 3 | - **CloudWatch Alarms & SNS Topics**: Tạo alarm riêng cho Lambda Errors, API Gateway 5xx, DLQ Depth (Critical) và Bedrock Throttle (Critical); tạo 2 SNS topic `alerts-info` và `alerts-critical`, subscribe email test. | 28/07/2026 | 28/07/2026 | AWS SNS & CloudWatch Alarms |
| 4 | - **AWS Chatbot & Tích hợp Slack**: Kết nối AWS Chatbot với Slack Workspace (OAuth authorize), route topic `alerts-critical` vào channel `#rag-alerts`; test gửi thông báo bằng lỗi Lambda giả lập. | 29/07/2026 | 29/07/2026 | AWS Chatbot Guide |
| 5 | - Tìm hiểu framework **RAGAS** (Faithfulness, Answer Relevancy, Context Precision) và EventBridge Scheduler; tạo rule chạy hàng ngày lúc 2h sáng trigger Lambda đánh giá. | 30/07/2026 | 30/07/2026 | RAGAS Framework Docs |
| 6 | - Viết Lambda **RAGAS Evaluation Runner**: Lấy mẫu ~20 cặp câu hỏi/câu trả lời từ ChatHistory 24h gần nhất, chấm điểm theo 3 chỉ số, lưu kết quả JSON vào S3 Evaluation Results; chạy thử và tổng hợp tiến độ. | 31/07/2026 | 31/07/2026 | Internal Test & Evaluation |

### Kết quả đạt được tuần 6:

* **Hệ thống quan sát trực quan (Observability)**: Xây dựng thành công CloudWatch Dashboard theo dõi toàn bộ tài nguyên Serverless, đẩy Custom Metrics trực tiếp từ Lambda code.
* **Cảnh báo sự cố chủ động qua Slack**: Thiết lập CloudWatch Alarms phân tầng thông qua SNS Topics và AWS Chatbot, tự động đẩy alert sự cố critical tức thì vào channel Slack `#rag-alerts`.
* **Tự động hóa đánh giá RAG (RAGAS Evaluation Pipeline)**: Triển khai thành công Lambda Evaluation Runner kết hợp EventBridge Scheduler chạy định kỳ 2h sáng, tự động lấy mẫu hội thoại và tính toán điểm số Faithfulness, Answer Relevancy, Context Precision xuất báo cáo JSON trên S3.
