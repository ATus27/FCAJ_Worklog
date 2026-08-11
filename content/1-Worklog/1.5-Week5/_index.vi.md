---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Triển khai API Gateway (REST API, CORS) kết hợp xác thực người dùng qua Amazon Cognito User Pool.
* Tích hợp Amazon ElastiCache (Semantic Cache với cosine similarity) để tối ưu chi phí và thời gian phản hồi.
* Thiết kế bảng DynamoDB (ChatHistory, FeedbackStore) và thiết lập Bedrock Guardrails (lọc chủ đề nhạy cảm, mask PII).
* Hoàn thiện và kiểm thử Luồng 2 (Realtime QA Pipeline) end-to-end trên Postman.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Triển khai Amazon API Gateway (REST API), bật CORS và tích hợp xác thực người dùng qua Amazon Cognito User Pool. | 20/07/2026 | 20/07/2026 | AWS API Gateway & Cognito Docs |
| 3 | - Tích hợp Amazon ElastiCache (Redis) làm lớp Semantic Cache, áp dụng độ tương đồng Cosine (Cosine Similarity) để giảm latency và chi phí gọi LLM. | 21/07/2026 | 21/07/2026 | AWS ElastiCache Developer Guide |
| 4 | - Thiết kế và khởi tạo các bảng Amazon DynamoDB: `ChatHistory` (lưu vết lịch sử hội thoại) và `FeedbackStore` (lưu đánh giá người dùng). | 22/07/2026 | 22/07/2026 | Amazon DynamoDB Docs |
| 5 | - Xây dựng và thiết lập Amazon Bedrock Guardrails: định nghĩa bộ lọc chủ đề nhạy cảm, ẩn/mask dữ liệu cá nhân (PII) và ngăn chặn Prompt Injection. | 23/07/2026 | 23/07/2026 | Amazon Bedrock Guardrails Guide |
| 6 | - Tích hợp toàn bộ Luồng 2 và tiến hành kiểm thử end-to-end bằng Postman (kiểm tra Token Auth, Hit/Miss Semantic Cache, Bedrock Guardrails). | 24/07/2026 | 24/07/2026 | Postman API Testing |

### Kết quả đạt được tuần 5:

* **Bảo mật & Quản lý người dùng qua API**: Thiết lập REST API Gateway chuẩn hóa có xác thực Cognito User Pool và hỗ trợ CORS cho ứng dụng Web.
* **Tối ưu hóa hiệu năng & Chi phí**: Tích hợp thành công Semantic Cache trên Amazon ElastiCache, giúp các câu hỏi trùng/tương đương được phản hồi tức thì mà không cần gọi Bedrock LLM.
* **Bảo vệ dữ liệu & Quản lý hội thoại**: Áp dụng Bedrock Guardrails lọc bỏ PII/nội dung độc hại, đồng thời lưu trữ đầy đủ lịch sử trò chuyện và feedback trên DynamoDB.
* **Nghiệm thu Luồng 2**: Kiểm thử thành công toàn bộ luồng hỏi đáp thời gian thực qua Postman với độ chính xác cao và thời gian phản hồi ấn tượng.
