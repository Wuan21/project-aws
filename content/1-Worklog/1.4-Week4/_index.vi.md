---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
### Mục tiêu tuần 4:

* Hiểu dịch vụ Amazon RDS và các tính năng nổi bật.
* Triển khai Amazon RDS MySQL trong private subnet.
* Kết nối ứng dụng Node.js với RDS và xác minh hoạt động database.
* Thực hành backup tự động, manual snapshot và point-in-time restore.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Amazon RDS: các engine hỗ trợ (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora) <br> - Tìm hiểu các tùy chọn triển khai: Single-AZ, Multi-AZ, Read Replica <br> - Tìm hiểu giá RDS: loại instance, storage (gp3, io1), data transfer <br> - Tìm hiểu Parameter Group và Option Group | 11/05/2026 | 11/05/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/> |
| 3   | - **Thực hành:** Tạo RDS MySQL 8.0 <br>&emsp; + Tạo DB Subnet Group (private subnet trên 2 AZ) <br>&emsp; + Tạo RDS với Multi-AZ, storage gp3 <br>&emsp; + Cấu hình Security Group: cho phép MySQL port 3306 từ Security Group của EC2 <br>&emsp; + Bật automated backup (7 ngày lưu trữ) và maintenance window | 12/05/2026 | 12/05/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/USER_CreateDBInstance.html> |
| 4   | - **Thực hành:** Kết nối ứng dụng với RDS <br>&emsp; + SSH vào EC2, cài MySQL client <br>&emsp; + Kết nối đến RDS endpoint, tạo database và bảng <br>&emsp; + Cập nhật biến môi trường Node.js (DB_HOST, DB_NAME, DB_USER, DB_PASS) <br>&emsp; + Test thao tác CRUD từ app đến RDS <br> - Bật RDS Enhanced Monitoring và Performance Insights | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu chiến lược backup và khôi phục RDS <br> - **Thực hành:** Backup và Restore <br>&emsp; + Tạo manual DB snapshot <br>&emsp; + Chỉnh sửa dữ liệu để mô phỏng thay đổi <br>&emsp; + Khôi phục RDS từ snapshot sang instance mới <br>&emsp; + Kiểm tra tính nhất quán dữ liệu sau khi restore | 14/05/2026 | 14/05/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/USER_RestoreFromSnapshot.html> |
| 6   | - **Thực hành:** Test failover RDS Multi-AZ <br>&emsp; + Kích hoạt manual failover qua console <br>&emsp; + Đo thời gian failover (DNS propagation) <br>&emsp; + Xác minh ứng dụng tự kết nối lại <br> - Tạo Read Replica ở AZ khác <br> - Xem lại chi phí và tối ưu cài đặt storage autoscaling | 15/05/2026 | 15/05/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/Concepts.MultiAZ.html> |


### Kết quả đạt được tuần 4:

* Hiểu Amazon RDS: các engine, Multi-AZ, Read Replica và automated backup.

* Triển khai RDS MySQL 8.0 trong private subnet với Multi-AZ đảm bảo high availability.

* Bảo mật truy cập database bằng Security Group chỉ cho phép từ application tier EC2.

* Kết nối ứng dụng Node.js với RDS, xác minh đầy đủ các thao tác CRUD.

* Tạo manual snapshot, restore database và xác minh tính toàn vẹn dữ liệu.

* Trigger và đo thời gian failover Multi-AZ, xác nhận ứng dụng tự kết nối lại.