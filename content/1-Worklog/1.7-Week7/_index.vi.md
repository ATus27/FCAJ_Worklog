---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Cải thiện chất lượng Retrieval (Hybrid Search OpenSearch & Chunking Size tuning).
* Kiểm thử tải sơ bộ API Gateway và rà soát IAM Policy theo nguyên tắc least privilege.
* Hoàn thiện cấu trúc Terraform & IaC (tách module, import resource, viết README).
* Soạn thảo tài liệu vận hành (Runbook), slide thuyết trình và thực hiện Demo chính thức trước nhóm.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Cải thiện chất lượng Retrieval**: Điều chỉnh tỷ lệ Hybrid Search trong OpenSearch (tăng trọng số vector search so với BM25 từ 50/50 lên 70/30); giảm kích thước chunk từ 300 xuống 200 token; chạy lại 5 câu hỏi từng bị điểm thấp — 4/5 câu cải thiện rõ rệt. | 03/08/2026 | 03/08/2026 | OpenSearch & Vector Search Docs |
| 3 | - **Kiểm thử tải sơ bộ & Security Review**: Thực hiện load test (50 request đồng thời tới API Gateway) và rà soát lại toàn bộ IAM Policy theo nguyên tắc least privilege lần cuối trước khi hoàn thiện. | 04/08/2026 | 04/08/2026 | AWS IAM & Load Testing Guide |
| 4 | - **Hoàn thiện Terraform & IaC**: Dọn dẹp mã, tách module rõ ràng theo từng luồng (ingestion, chat-api, monitoring, evaluation), import ngược các resource từng tạo thủ công qua Console vào Terraform state, viết README hướng dẫn deploy từ đầu. | 05/08/2026 | 05/08/2026 | Terraform Docs & Best Practices |
| 5 | - **Viết tài liệu vận hành & Runbook**: Mô tả kiến trúc tổng thể, hướng dẫn xử lý khi có alert (ví dụ DLQ Depth > 0), checklist bảo trì định kỳ; chuẩn bị slide và kịch bản demo cho buổi trình bày cuối kỳ. | 06/08/2026 | 06/08/2026 | Project Runbook & Presentation |
| 6 | - **Demo chính thức trước nhóm**: Chạy trực tiếp từ upload tài liệu ➔ hỏi đáp ➔ xem alert giả lập ➔ xem báo cáo RAGAS; ghi nhận góp ý và tổng kết lại toàn bộ hành trình 5 tuần cùng hướng phát triển tiếp theo. | 07/08/2026 | 07/08/2026 | Team Review & Demo |

### Kết quả đạt được tuần 7:

* **Tối ưu hóa độ chính xác Retrieval**: Tăng đáng kể chất lượng câu trả lời bằng cách tinh chỉnh trọng số Hybrid Search (70/30) và thu nhỏ Chunk Size xuống 200 tokens.
* **Chuẩn hóa Infrastructure as Code**: Tách biệt mã nguồn Terraform thành 4 module độc lập, import 100% tài nguyên thủ công vào IaC state và viết hướng dẫn triển khai từ đầu trong README.
* **Tài liệu vận hành & Demo thành công**: Xây dựng Runbook chi tiết hướng dẫn ứng phó sự cố và trình bày thành công Demo sản phẩm mượt mà trước nhóm/mentor.
