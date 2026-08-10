---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Triển khai Luồng 2 (Hỏi đáp Realtime): Xây dựng bộ nhớ đệm ngữ nghĩa Semantic Cache với ElastiCache Serverless.
* Tích hợp tìm kiếm Vector k-NN trên OpenSearch Serverless và sinh câu trả lời tự nhiên với Amazon Bedrock (Claude 3).
* Cấu hình Amazon Bedrock Guardrails, lưu trữ Chat History trên DynamoDB và bảo mật Endpoint bằng API Gateway & Cognito.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Triển khai **Amazon ElastiCache Serverless** (Redis) làm lớp **Semantic Cache**.<br>- Xây dựng cơ chế tính Embedding câu hỏi mới ➔ So sánh khoảng cách vector trong Redis Cache. Nếu khớp câu hỏi cũ (Similarity >= 0.90) ➔ Trả về câu trả lời ngay lập tức (Bypass LLM). | 27/07/2026 | 27/07/2026 | Workshop Section 5.4 |
| 3 | - Nếu Cache Miss: Thực hiện Vector Search k-NN trên OpenSearch Serverless dựa vào embedding câu hỏi ➔ Trích xuất Top-K đoạn ngữ cảnh (context) liên quan nhất. | 28/07/2026 | 28/07/2026 | Workshop Section 5.4 |
| 4 | - Tích hợp **Amazon Bedrock (Claude 3 Haiku / Sonnet)** để tạo câu trả lời dựa trên ngữ cảnh đã trích xuất.<br>- Cấu hình **Amazon Bedrock Guardrails**: Thiết lập PII Redaction, Topic Blocking, Content Filtering và chống Prompt Injection. | 29/07/2026 | 29/07/2026 | Workshop Section 5.4 |
| 5 | - Tạo bảng **Amazon DynamoDB** lưu lịch sử hội thoại (Chat History) theo `SessionId` và `Timestamp`.<br>- Triển khai **Amazon API Gateway** + **Amazon Cognito User Pool** để bảo mật các Endpoint API hỏi đáp. | 30/07/2026 | 30/07/2026 | Workshop Section 5.4 |
| 6 | - **Kiểm thử Luồng 2**: Gửi câu hỏi qua Postman/AWS CLI, kiểm tra tốc độ phản hồi khi Hit Cache vs. Miss Cache, thử nghiệm nhập prompt độc hại để kiểm tra Bedrock Guardrails. | 31/07/2026 | 31/07/2026 | Workshop Section 5.4 & 5.10 |

### Kết quả đạt được tuần 6:

* **Tối ưu hóa hiệu năng & Chi phí với Semantic Cache**: Thiết lập bộ đệm ngữ nghĩa trên ElastiCache Serverless giúp phản hồi các câu hỏi lặp lại tức thì và tiết kiệm chi phí gọi LLM.
* **Xây dựng RAG Pipeline hoàn chỉnh**: Kết nối thành công Vector Retrieval từ OpenSearch Serverless với mô hình Claude 3 trên Bedrock.
* **Bảo mật & Kiểm soát nội dung**: Thiết lập lớp Bedrock Guardrails chống rò rỉ dữ liệu PII / Prompt Injection, đồng thời quản lý lịch sử hội thoại trên DynamoDB và xác thực qua Cognito API Gateway.
