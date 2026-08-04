---
title: "Worklog Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:
* Kết nối, làm quen với các thành viên trong First Cloud AI Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI, bắt đầu học về "Hành trình lên mây".
* Tạo tài khoản và làm nhiệm vụ lấy 200$ credits AWS
### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Lên văn phòng ngày đầu tiên <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập                                                                                             | 22/06/2026   | 22/06/2026      |
| 3   | - Làm việc tại văn phòng ngày 2<br> - Tạo tài khoản AWS console, thu thập credits, vào nhóm làm việc Tên nhóm: SGU_RAGonAWS                                           | 23/06/2026   | 23/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Bắt đầu tìm hiểu về AWS console và thu thập credit <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thực hành:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI <br> - **Thu thập credit:** <br>&emsp; + Task 1: Launch EC2 Instance - $20 credit <br>&emsp; + Task 2: Amazon Bedrock Playground - $20 credit | 24/06/2026   | 24/06/2026      | https://000001.awsstudygroup.com/vi/|
| 5   | - **Thu thập credit:** <br>&emsp; + Task 3: Set up AWS Budgets - $20 credit <br>&emsp; + Task 4: Create Lambda Web App - $20 credit <br>&emsp; + Task 5: Create RDS Database - $20 credit | 25/06/2026   | 26/06/2026      | https://000001.awsstudygroup.com/vi/ |
| 6   | - Tìm hiểu tiếp các mục còn lại trong tài liệu hướng dẫn: <br>&emsp; + Mục 5: Danh sách "sát thủ" credit cần tránh <br>&emsp; + Mục 6: Kiến trúc mẫu với $200 credit <br>&emsp; + Mục 7: Monitoring và tối ưu chi phí <br>&emsp; + Mục 8: FAQ - Giải đáp mọi thắc mắc <br>&emsp; + Mục 9: Roadmap học AWS với Free Tier <br>&emsp; + Mục 10: Tổng kết và Next Steps | 26/06/2026   | 26/06/2026      | https://000001.awsstudygroup.com/vi/ |


### Kết quả đạt được tuần 1:

#### 1. Thiết lập tài khoản & Chiến lược tích lũy $200 credit:
*   Đã khởi tạo thành công tài khoản **AWS Free Tier** mới (áp dụng cho các tài khoản tạo sau ngày 15/07/2025).
*   Hiểu rõ chiến lược nhận đủ **$200 credit** (gồm $100 mặc định ban đầu và $100 tích lũy từ 5 nhiệm vụ "kiếm tiền").

#### 2. Thực hành chi tiết 5 nhiệm vụ tích lũy credit:
*   **Task 1: Launch EC2 Instance**: Tạo máy ảo EC2 (`Test Instance`), cấu hình Key Pair (`first-kp`), Security Group và thực hiện Terminate dọn dẹp để bảo toàn tài nguyên.
*   **Task 2: Amazon Bedrock Playground**: Trải nghiệm AI/ML với model **Claude 3 Haiku** trong Bedrock Playground. Nắm rõ quy trình gửi Ticket Support kích hoạt quyền truy cập model (Bedrock Allowlisting) khi gặp lỗi phân quyền.
*   **Task 3: Set up AWS Budgets**: Cấu hình cơ bản bộ giám sát và cảnh báo chi phí trực quan thông qua giao diện Budgets.
*   **Task 4: Create Lambda Web App**: Xây dựng serverless web application cơ bản từ Blueprint (`Getting started with Lambda HTTP`) và thực hành xóa function an toàn.
*   **Task 5: Create RDS Database**: Khởi tạo RDS Database Cluster (Aurora PostgreSQL Compatible) thông qua Easy Create và quy trình dọn dẹp, xóa DB cluster cùng instance tránh phát sinh chi phí.

#### 3. Kiểm soát tài khoản & Nhận diện "sát thủ" chi phí:
*   Nhận diện các dịch vụ đắt đỏ có khả năng làm cạn kiệt credit nhanh chóng: **Amazon SageMaker** (Training Jobs, Notebook, Endpoints), **GPU Instances** (p3, p4d, g4dn), và **Amazon Redshift**.
*   Thiết lập bộ cảnh báo ngân sách phòng thủ **My-200$-budget** định kỳ hàng tháng với 4 mức ngưỡng cảnh báo chi phí chi tiết (`$12.5`, `$25`, `$50`, `$75`) qua Email.
*   Phân biệt nhóm dịch vụ luôn an toàn (Always Safe) như *Lambda, DynamoDB, S3, CloudWatch, SNS, SES* và nhóm dịch vụ an toàn có điều kiện (t2/t3.micro cho EC2, db.t3.micro cho RDS).

#### 4. Phân tích & Lựa chọn kiến trúc tối ưu:
*   Nghiên cứu 2 mô hình kiến trúc mẫu trong hạn mức $200 credit:
    *   **Simple Web Application**: Dự kiến tiêu tốn ~$80-120/6 tháng (sử dụng CloudFront, S3, ALB, EC2 t3.micro, RDS db.t3.micro).
    *   **Serverless Application**: Mô hình tối ưu chi phí tối đa chỉ khoảng ~$60/6 tháng (sử dụng CloudFront, Amplify, Lambda, Bedrock Haiku, DynamoDB, Cognito).

#### 5. Khung giám sát chi phí nâng cao (Cost Optimization Framework):
*   Nắm vững quy trình Cost Monitoring cơ bản bằng AWS Budgets, Billing Alerts và Cost Explorer hàng ngày.
*   Hiểu chiến lược sử dụng kịch bản tự động hóa dọn dẹp tài nguyên (Automated Cleanup Script) qua AWS CLI và chiến lược gắn thẻ tài nguyên (Resource Tagging).
*   Thực hành giao thức xử lý khẩn cấp (Emergency Cost Control) khi chi tiêu vượt quá $150 thông qua các câu lệnh AWS CLI để tìm tài nguyên đắt đỏ nhất và dừng khẩn cấp các instance không quan trọng.


