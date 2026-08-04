---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Làm chủ cả lý thuyết và kỹ năng thực hành cấu hình mạng ảo AWS VPC, thiết lập tường lửa bảo mật, triển khai máy chủ ảo an toàn và xây dựng các kết nối nâng cao (Transit Gateway, VPN) thông qua chuỗi bài Lab thực tế.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **VPC Nền tảng, Subnet & Sơ đồ mạng cơ bản**<br>&emsp; + **Lý thuyết:** Học về VPC, phân tách Subnet (Public/Private), Route Table, card mạng ảo ENI và địa chỉ Elastic IP.<br>&emsp; + **Thực hành (Lab):** Khởi tạo VPC, chia Subnets, tạo Internet Gateway (IGW) và liên kết bảng định tuyến. | 29/06/2026 | 29/06/2026 | • Video *Module 02-01*<br>• Workshop *Section 1 & 3.1 - 3.4* |
| 3 | - **Tường lửa, Bảo mật & Giám sát VPC**<br>&emsp; + **Lý thuyết:** Phân biệt Security Groups (Stateful - cấp độ ENI) và Network ACLs (Stateless - cấp độ Subnet). Cách thức ghi nhật ký với VPC Flow Logs.<br>&emsp; + **Thực hành (Lab):** Tạo Security Group riêng cho Web/Database Server, thiết lập Network ACLs và kích hoạt VPC Flow Logs. | 30/06/2026 | 30/06/2026 | • Video *Module 02-02*<br>• Workshop *Section 2, 3.5 & 3.6* |
| 4 | - **NAT Gateway & Triển khai Máy chủ ảo EC2**<br>&emsp; + **Lý thuyết:** Cách thức hoạt động của NAT Gateway (kết nối internet 1 chiều từ Private Subnet) và VPC Endpoints.<br>&emsp; + **Thực hành (Lab):** Khởi tạo máy chủ EC2, kiểm tra kết nối bằng Reachability Analyzer. Cấu hình NAT Gateway cho Private Subnet và kết nối an toàn qua Systems Manager Session Manager. | 01/07/2026 | 01/07/2026 | • Video *Module 02-01*<br>• Workshop *Section 4.1 - 4.7* |
| 5 | - **Kết nối liên mạng (Multi-VPC) & Transit Gateway**<br>&emsp; + **Lý thuyết:** Tìm hiểu VPC Peering (kết nối 1-1 không bắc cầu) và Transit Gateway (mô hình Hub-and-Spoke cho doanh nghiệp lớn).<br>&emsp; + **Thực hành (Lab):** Thiết lập môi trường Transit Gateway, tạo Transit Gateway Attachment và cấu hình bảng định tuyến kết nối liên VPC. | 02/07/2026 | 02/07/2026 | • Video *Module 02-02*<br>• Workshop *Section 5.3* |
| 6 | - **Thiết lập AWS Site-to-Site VPN & Load Balancer**<br>&emsp; + **Lý thuyết:** Cách thức kết nối mạng Hybrid bằng AWS VPN và Direct Connect. Phân bổ lưu lượng bằng Elastic Load Balancing (ALB, NLB, GLB).<br>&emsp; + **Thực hành (Lab):** Tạo Virtual Private Gateway, Customer Gateway và cấu hình kết nối VPN Site-to-Site hoàn chỉnh. Tiến hành dọn dẹp tài nguyên tránh phát sinh chi phí. | 03/07/2026 | 03/07/2026 | • Video *Module 02-03*<br>• Workshop *Section 5.1 - 5.2 & Section 6* |

### Kết quả đạt được tuần 2:

* **Thiết lập hạ tầng chuẩn Production**: Biết cách tự tay xây dựng sơ đồ mạng VPC thực tế bao gồm cả multi-AZ và giám sát an toàn bằng Flow Logs.
* **Thành thạo kết nối nâng cao**: Có khả năng cấu hình liên mạng thông qua Transit Gateway và thiết lập đường truyền mã hóa an toàn AWS Site-to-Site VPN về môi trường on-premises.
* **Kiểm soát chi phí**: Biết cách tối ưu hóa tài nguyên mạng và hoàn thành quy trình dọn dẹp sạch sẽ sau khi thực hành xong để tránh các hóa đơn ngoài ý muốn từ AWS.
