---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
### Mục tiêu tuần 3:

* Quản lý EC2 Linux và Windows instance hiệu quả trong VPC.
* Triển khai ứng dụng web Node.js trên EC2 instance.
* Hiểu về tạo AMI, Launch Template và quản lý Elastic IP.
* Cấu hình Security Group và kiểm soát truy cập cho ứng dụng web.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu nâng cao về EC2: AMI lifecycle, Launch Template, Instance Metadata Service <br> - Ôn tập EC2 Windows: kết nối RDP, giải mã mật khẩu admin bằng key pair <br> - Tìm hiểu Placement Group (cluster, spread, partition) | 04/05/2026 | 04/05/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/> |
| 3   | - **Thực hành:** Khởi tạo và quản lý EC2 nhiều loại <br>&emsp; + Khởi tạo Amazon Linux 2 trong public subnet <br>&emsp; + Khởi tạo Windows Server 2022, lấy mật khẩu, kết nối RDP <br>&emsp; + So sánh quản lý instance giữa Linux và Windows <br>&emsp; + Tạo AMI tùy chỉnh từ instance Linux đã cấu hình | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Triển khai ứng dụng Node.js trên EC2 Linux <br>&emsp; + Cài Node.js (v18 LTS) qua nvm <br>&emsp; + Clone ứng dụng Express.js mẫu <br>&emsp; + Cấu hình biến môi trường (DB host, port, secrets) <br>&emsp; + Cài PM2 process manager và khởi động app <br>&emsp; + Cấu hình Security Group cho phép HTTP port 3000 | 06/05/2026 | 06/05/2026 | <https://nodejs.org/en/docs> |
| 5   | - Cấu hình Nginx làm reverse proxy cho Node.js: <br>&emsp; + Cài đặt và cấu hình Nginx <br>&emsp; + Proxy HTTP port 80 đến Node.js port 3000 <br>&emsp; + Cấu hình Security Group: cho phép HTTP (80) và HTTPS (443) <br> - Cấu hình PM2 tự khởi động lại app khi reboot <br> - Cấp phát Elastic IP và gắn vào instance | 07/05/2026 | 07/05/2026 | <https://www.nginx.com/resources/wiki/> |
| 6   | - **Thực hành:** Tạo Launch Template cho triển khai EC2 lặp lại <br>&emsp; + Cấu hình instance type, AMI, subnet, Security Group, user data script <br>&emsp; + User data: tự động cài Node.js và khởi động app khi boot <br> - Test ứng dụng end-to-end qua Elastic IP và Nginx <br> - Ghi lại tài liệu các bước triển khai | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 3:

* Khởi tạo và quản lý thành công EC2 Linux (Amazon Linux 2) và Windows Server (2022).

* Kết nối Linux qua SSH và Windows qua RDP sau khi giải mã mật khẩu administrator.

* Triển khai ứng dụng Node.js (Express.js) trên EC2 với PM2 làm process manager.

* Cấu hình Nginx làm reverse proxy, expose ứng dụng qua port 80.

* Tạo AMI tùy chỉnh và Launch Template với user data để tự động hóa triển khai.

* Gắn Elastic IP để đảm bảo endpoint ổn định cho ứng dụng web.