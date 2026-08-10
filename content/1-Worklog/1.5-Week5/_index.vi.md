---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Khởi tạo hạ tầng Vector Database với Amazon OpenSearch Serverless (AOSS).
* Thực hiện thuật toán phân đoạn văn bản (Text Chunking).
* Tích hợp Amazon Bedrock Titan Embeddings để tạo Vector 1536 chiều và lập chỉ mục (Indexing) vào OpenSearch Serverless (Hoàn thiện Luồng 1 - Data Ingestion).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu dịch vụ **Amazon OpenSearch Serverless (AOSS)** Vector Search Collection.<br>- Viết Terraform triển khai AOSS Collection, Security Policy, Encryption Policy và Network Access Policy.<br>- Cấu hình IAM Data Access Policy cho phép Lambda truy cập AOSS. | 20/07/2026 | 20/07/2026 | Workshop Section 5.3 |
| 3 | - Tìm hiểu chiến lược phân đoạn văn bản (**Chunking Strategy**): Overlapping Chunks, Fixed-size Chunking (ví dụ: 512 tokens, overlap 50 tokens).<br>- Lập trình module Chunking bằng Python trong Lambda. | 21/07/2026 | 21/07/2026 | Workshop Section 5.3 |
| 4 | - Tìm hiểu và tích hợp model **Amazon Titan Text Embeddings v1** (`amazon.titan-embed-text-v1`).<br>- Gọi API Bedrock trong Lambda để chuyển các đoạn văn bản thành các vector 1536 chiều. | 22/07/2026 | 22/07/2026 | Workshop Section 5.3 |
| 5 | - Tạo OpenSearch Vector Index với k-NN vector field type (Distance metric: Cosine / HNSW).<br>- Đẩy danh sách vector cùng metadata (source_file, chunk_id, text_content, page) vào OpenSearch Index. | 23/07/2026 | 23/07/2026 | Workshop Section 5.3 |
| 6 | - **Kiểm thử End-to-End Luồng 1**: Upload tài liệu phức tạp (file scan nhiều trang) ➔ Xác nhận dữ liệu vector được lập chỉ mục thành công trong OpenSearch Serverless. | 24/07/2026 | 24/07/2026 | Workshop Section 5.3 & 5.10 |

### Kết quả đạt được tuần 5:

* **Làm chủ Vector Database Serverless**: Triển khai thành công Amazon OpenSearch Serverless bằng Terraform kèm các chính sách bảo mật mạng và phân quyền dữ liệu (Data Access Policy).
* **Xử lý ngữ nghĩa dữ liệu**: Nắm vững kỹ thuật Text Chunking và tạo nhúng vector với Amazon Titan Embeddings v1 trên Bedrock.
* **Hoàn chỉnh Pipeline Ingestion**: Tự động hóa 100% quy trình từ khi upload tài liệu thô trên S3 cho đến khi dữ liệu được số hóa, vector hóa và lưu trữ sẵn sàng cho tìm kiếm ngữ nghĩa.
