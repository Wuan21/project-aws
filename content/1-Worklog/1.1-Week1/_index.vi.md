---
title: "Worklog Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---
### Mục tiêu tuần 1:

* Làm quen với các thành viên FCAJ và nắm rõ nội quy đơn vị thực tập.
* Hiểu AWS là gì và khám phá các nhóm dịch vụ chính.
* Tạo tài khoản AWS Free Tier và cấu hình AWS CLI.
* Thực hành khởi tạo và quản lý EC2 instance cơ bản.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Làm quen với các thành viên FCAJ <br> - Đọc và nắm nội quy, quy định tại đơn vị thực tập <br> - Tổng quan về AWS: lịch sử, hạ tầng toàn cầu, Shared Responsibility Model | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu sâu các nhóm dịch vụ AWS: <br>&emsp; + Compute: EC2, Lambda, ECS <br>&emsp; + Storage: S3, EBS, EFS, Glacier <br>&emsp; + Networking: VPC, CloudFront, Route 53 <br>&emsp; + Database: RDS, DynamoDB, ElastiCache <br>&emsp; + Security: IAM, KMS, CloudTrail | 21/04/2026 | 21/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo tài khoản AWS Free Tier <br> - Khám phá AWS Management Console <br> - **Thực hành:** <br>&emsp; + Cài đặt và cấu hình AWS CLI v2 <br>&emsp; + Cấu hình credentials (Access Key, Secret Key, Region, Output format) <br>&emsp; + Chạy lệnh CLI cơ bản: list regions, describe instances, list S3 buckets | 22/04/2026 | 22/04/2026 | <https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Các loại instance và họ instance (t3, m5, c5, r5) <br>&emsp; + Amazon Machine Images (AMI) – public, community, private <br>&emsp; + EBS volumes (gp3, io1, st1) và snapshot <br>&emsp; + Key pair và các phương thức kết nối SSH <br>&emsp; + Elastic IP và vòng đời public IP | 23/04/2026 | 23/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Khởi tạo EC2 Amazon Linux 2 (t3.micro) <br>&emsp; + Cấu hình Security Group (cho phép SSH port 22) <br>&emsp; + Kết nối instance qua SSH bằng key pair <br>&emsp; + Gắn và mount EBS volume <br>&emsp; + Cấp phát và gắn Elastic IP | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 1:

* Hiểu mục đích của AWS, hạ tầng toàn cầu (Region, Availability Zone, Edge Location) và Shared Responsibility Model.

* Nắm được các nhóm dịch vụ chính: Compute, Storage, Networking, Database và Security.

* Tạo và cấu hình thành công tài khoản AWS Free Tier.

* Cài đặt AWS CLI v2, cấu hình Access Key, Secret Key, Region mặc định và output format.

* Thực hiện các thao tác CLI: liệt kê region, xem EC2 instance, liệt kê S3 bucket, quản lý key pair.

* Khởi tạo EC2 Amazon Linux 2, kết nối SSH, gắn EBS volume và cấu hình Elastic IP.