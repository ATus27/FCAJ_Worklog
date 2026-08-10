---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Triển khai Luồng 3 (Monitoring & Alert): Xây dựng CloudWatch Dashboards, Log Metrics, Alarms và gửi thông báo cảnh báo tự động về Slack thông qua Amazon SNS & AWS Chatbot.
* Triển khai Luồng 4 (RAGAS Evaluation): Tự động đo lường chất lượng câu trả lời RAG (Faithfulness, Relevance, Recall, Precision) bằng Lambda & EventBridge Scheduler.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Luồng 3 - Giám sát**: Tạo CloudWatch Log Groups, Log Metric Filters cho Lambda, API Gateway và OpenSearch.<br>- Xây dựng **CloudWatch Dashboard** trực quan hiển thị: Total Requests, Latency (p95, p99), Cache Hit Ratio, Error Count, Token Costs. | 03/08/2026 | 03/08/2026 | Workshop Section 5.5 |
| 3 | - Thiết lập **CloudWatch Alarms** (Cảnh báo khi SQS DLQ > 0, Lambda Error Rate > 5%, API Gateway Latency cao).<br>- Triển khai **Amazon SNS** tích hợp **AWS Chatbot** gửi thông báo sự cố tự động về kênh Slack của nhóm. | 04/08/2026 | 04/08/2026 | Workshop Section 5.5 |
| 4 | - **Luồng 4 - Đánh giá RAGAS**: Tìm hiểu thư viện RAGAS đánh giá 4 chỉ số: *Faithfulness*, *Answer Relevance*, *Context Precision*, *Context Recall*.<br>- Chuẩn bị bộ Test Dataset (Ground Truth Test Set) gồm các cặp câu hỏi - đáp tiêu chuẩn. | 05/08/2026 | 05/08/2026 | Workshop Section 5.6 |
| 5 | - Viết Lambda Function làm **RAGAS Evaluation Runner**.<br>- Triển khai **Amazon EventBridge Scheduler** lập lịch kích hoạt RAGAS Runner chạy đánh giá tự động hàng ngày. | 06/08/2026 | 06/08/2026 | Workshop Section 5.6 |
| 6 | - Lưu trữ kết quả đánh giá chỉ số RAGAS dưới dạng file JSON/CSV lên S3 Evaluation Bucket.<br>- Phân tích báo cáo RAGAS đầu tiên để tinh chỉnh lại tham số Top-K Retrieval & Prompt Templates. | 07/08/2026 | 07/08/2026 | Workshop Section 5.6 & 5.10 |

### Kết quả đạt được tuần 7:

* **Khả năng quan sát toàn diện (Observability)**: Xây dựng hệ thống giám sát tập trung trên CloudWatch Dashboard và thiết lập cơ chế cảnh báo chủ động tới kênh Slack qua SNS & AWS Chatbot.
* **Đánh giá chất lượng RAG tự động**: Tự động hóa 100% quy trình đánh giá độ chính xác, độ tin cậy của câu trả lời với khung RAGAS và EventBridge Scheduler.
* **Cải thiện hệ thống dựa trên dữ liệu**: Nhận diện các điểm yếu trong retrieval context để tối ưu lại prompt và số lượng Top-K chunks lấy về.
