---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Xây dựng giao diện Frontend (React / Web UI) và tích hợp hoàn thiện với Backend API Gateway & Cognito.
* Lập đường ống CI/CD tự động hóa kiểm thử và triển khai bằng GitHub Actions / AWS CodePipeline.
* Kiểm thử toàn bộ hệ thống (End-to-End Testing), rà soát bảo mật, đóng gói báo cáo dự án và chuẩn bị quy trình dọn dẹp tài nguyên (Resource Cleanup).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Frontend**: Triển khai giao diện người dùng (React / Web App).<br>- Tích hợp trang Đăng nhập / Đăng ký kết nối Amazon Cognito User Pool.<br>- Thiết lập giao diện Upload tài liệu và Chatbot UI hiển thị phản hồi thời gian thực. | 10/08/2026 | 10/08/2026 | Workshop Section 5.7 |
| 3 | - **Backend Integration**: Kết nối Frontend với API Gateway.<br>- Xử lý luồng hiển thị Citation (Nguồn trích dẫn trang tài liệu) dưới mỗi câu trả lời.<br>- Quản lý Token Auth trong LocalStorage / Cookie bảo mật. | 11/08/2026 | 11/08/2026 | Workshop Section 5.8 |
| 4 | - **Xây dựng CI/CD Pipeline**: Viết GitHub Actions / AWS CodePipeline workflow.<br>- Tự động kiểm tra cú pháp Terraform (`terraform fmt`, `validate`), chạy linter Python và deploy hạ tầng khi push code lên nhánh `main`. | 12/08/2026 | 12/08/2026 | Workshop Section 5.9 |
| 5 | - **System Testing (E2E)**: Kiểm thử toàn bộ 4 luồng xử lý từ Upload file ➔ Indexing ➔ Realtime QA ➔ Cache ➔ Cảnh báo Slack ➔ Đánh giá RAGAS.<br>- Đo lường hiệu năng tổng thể và rà soát bảo mật IAM Roles. | 13/08/2026 | 13/08/2026 | Workshop Section 5.10 |
| 6 | - **Quy trình dọn dẹp (Cleanup)**: Đóng gói script `terraform destroy` và quy trình xóa S3 Objects / AOSS Collections an toàn.<br>- Tổng kết toàn bộ báo cáo dự án, quay video Demo sản phẩm và hoàn thiện Worklog. | 14/08/2026 | 14/08/2026 | Workshop Section 5.11 |

### Kết quả đạt được tuần 8:

* **Sản phẩm hoàn chỉnh (Production-ready)**: Hoàn thiện ứng dụng RAG Knowledge Assistant với giao diện người dùng thân thiện, tích hợp đầy đủ xác thực bảo mật và hiển thị trích dẫn nguồn tài liệu.
* **Tự động hóa CI/CD**: Xây dựng thành công đường ống CI/CD kiểm thử và triển khai hạ tầng dạng mã nguồn tự động qua GitHub Actions / CodePipeline.
* **Nghiệm thu & Quản lý vòng đời tài nguyên**: Hoàn thành kiểm thử End-to-End thành công, nghiệm thu các chỉ số RAGAS và nắm rõ quy trình dọn dẹp hạ tầng an toàn với Terraform (`terraform destroy`).
