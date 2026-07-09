---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
### Mục tiêu tuần 2:

* Hiểu kiến trúc VPC: CIDR, subnet, routing và các loại gateway.
* Thiết kế và triển khai VPC hoàn chỉnh với public và private subnet trên nhiều AZ.
* Cấu hình Security Group, NACL, Internet Gateway và NAT Gateway.
* Xác minh kết nối giữa các subnet và kết nối internet từ instance.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu VPC cơ bản: CIDR block, địa chỉ IPv4/IPv6 <br> - Phân biệt subnet public và private, route table và availability zone <br> - So sánh Default VPC và Custom VPC | 27/04/2026 | 27/04/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/> |
| 3   | - **Thực hành:** Tạo Custom VPC (10.0.0.0/16) <br>&emsp; + Tạo 2 public subnet ở 2 AZ khác nhau (10.0.1.0/24, 10.0.2.0/24) <br>&emsp; + Tạo 2 private subnet ở 2 AZ khác nhau (10.0.3.0/24, 10.0.4.0/24) <br>&emsp; + Gắn Internet Gateway vào VPC <br>&emsp; + Cấu hình route table public: route 0.0.0.0/0 đến IGW | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Cấu hình internet ra cho private subnet <br>&emsp; + Tạo NAT Gateway trong public subnet với Elastic IP <br>&emsp; + Cập nhật route table private: route 0.0.0.0/0 đến NAT Gateway <br>&emsp; + Cấu hình Security Group: cho phép HTTP/HTTPS từ ALB, SSH từ bastion host <br>&emsp; + Cấu hình Network ACL bảo vệ cấp subnet | 29/04/2026 | 29/04/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html> |
| 5   | - Triển khai bastion host (EC2) trong public subnet <br> - Khởi tạo EC2 trong private subnet <br> - Xác minh SSH: máy local → bastion → instance private <br> - Kiểm tra internet outbound từ private instance qua NAT Gateway | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Xem lại và hoàn thiện sơ đồ kiến trúc VPC <br> - **Thực hành:** Bật VPC Flow Logs đến CloudWatch Logs <br>&emsp; + Tạo Flow Log cho VPC <br>&emsp; + Truy vấn flow log để phân tích traffic <br> - Ghi lại tài liệu thiết kế VPC đầy đủ | 01/05/2026 | 01/05/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html> |


### Kết quả đạt được tuần 2:

* Thiết kế và triển khai VPC theo chuẩn production với public và private subnet trên 2 Availability Zone.

* Cấu hình Internet Gateway và NAT Gateway cho phép truy cập internet đúng hướng từ mỗi loại subnet.

* Bảo mật tài nguyên bằng Security Group (cấp instance) và Network ACL (cấp subnet).

* Triển khai bastion host và kết nối thành công vào EC2 private qua SSH jump.

* Bật và truy vấn VPC Flow Logs trong CloudWatch để phân tích lưu lượng mạng.

* Xác minh đầy đủ kết nối: public subnet đến internet, private subnet qua NAT, và giữa các subnet với nhau.