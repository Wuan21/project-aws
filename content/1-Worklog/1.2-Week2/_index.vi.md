---
title: "Tuần 2: Tìm hiểu EC2, VPC và AWS Lambda"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
### Mục tiêu tuần 2:

* Tìm hiểu tổng quan về Amazon EC2 và vai trò của nó như một máy chủ ảo trên cloud.
* Tìm hiểu về Amazon VPC và các thành phần mạng cốt lõi của nó.
* Tìm hiểu về AWS Lambda và mô hình serverless computing.
* So sánh EC2 và Lambda trong các trường hợp sử dụng khác nhau.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu Amazon EC2: khái niệm, mục đích và vai trò như máy chủ ảo trên cloud <br> - Tìm hiểu loại instance và họ instance EC2 (t3, m5, c5, r5) <br> - Hiểu Amazon Machine Images (AMI) và cách chúng được dùng để khởi tạo instance | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Thực hành:** Tạo và cấu hình EC2 instance cơ bản <br>&emsp; + Khởi tạo Amazon Linux 2 instance (t3.micro) <br>&emsp; + Cấu hình Security Group cho phép SSH <br>&emsp; + Kết nối instance qua SSH bằng key pair <br>&emsp; + Khám phá cài đặt instance: loại instance, lưu trữ, mạng và tags | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Nghiên cứu Amazon VPC và các thành phần cốt lõi: <br>&emsp; + Subnet: public và private subnet <br>&emsp; + Route Table: định tuyến traffic trong và ngoài VPC <br>&emsp; + Internet Gateway: cho phép truy cập internet từ public subnet <br>&emsp; + Security Group và Network ACL: kiểm soát traffic vào và ra | 29/04/2026 | 29/04/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/> |
| 5   | - Hiểu cách VPC giúp cô lập và quản lý tài nguyên mạng trên AWS <br> - Nghiên cứu AWS Lambda: khái niệm, mô hình thực thi, trigger và mô hình serverless <br> - Tìm hiểu sự khác biệt giữa Lambda và EC2 về quản lý hạ tầng và tính phí | 30/04/2026 | 30/04/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/> |
| 6   | - **Thực hành:** Tạo Lambda function đơn giản <br>&emsp; + Tạo Lambda function dùng runtime Python hoặc Node.js <br>&emsp; + Viết handler cơ bản trả về response <br>&emsp; + Test function bằng Lambda console test event <br>&emsp; + So sánh EC2 và Lambda: use case, mô hình chi phí và overhead quản lý | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Nắm vững Amazon EC2 như dịch vụ máy chủ ảo, bao gồm loại instance, AMI và các tùy chọn cấu hình chính.

* Tạo và cấu hình thành công EC2 instance cơ bản, kết nối SSH và khám phá cài đặt mạng và lưu trữ.

* Tìm hiểu Amazon VPC và các thành phần cốt lõi: subnet, route table, internet gateway và security group, hiểu cách chúng cô lập và quản lý mạng đám mây.

* Nghiên cứu AWS Lambda và mô hình serverless, tìm hiểu cách Lambda loại bỏ nhu cầu quản lý hạ tầng máy chủ.

* Tạo Lambda function đơn giản và kiểm thử trên AWS Console.

* So sánh EC2 và Lambda, hiểu được các trường hợp sử dụng phù hợp cho từng dịch vụ compute.