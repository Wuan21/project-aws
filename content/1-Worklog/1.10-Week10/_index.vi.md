---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---
### Mục tiêu tuần 10:

* Kết nối nhiều VPC bằng VPC Peering và AWS Transit Gateway.
* Hiểu định tuyến và các hệ quả bảo mật của kiến trúc multi-VPC.
* Tự động hóa các tác vụ vận hành bằng AWS Lambda và Amazon EventBridge.
* Xây dựng workflow hướng sự kiện cho tự động hóa theo lịch và phản ứng sự kiện.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu VPC Peering: cách hoạt động, yêu cầu định tuyến, giới hạn (không có transitive routing) <br> - Tìm hiểu AWS Transit Gateway: attachment, route table, hub định tuyến tập trung <br> - So sánh VPC Peering và Transit Gateway: quy mô, chi phí, trường hợp sử dụng | 22/06/2026 | 22/06/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/> |
| 3   | - **Thực hành:** VPC Peering <br>&emsp; + Tạo VPC thứ hai (10.1.0.0/16) với private subnet <br>&emsp; + Tạo kết nối VPC Peering giữa VPC-A và VPC-B <br>&emsp; + Chấp nhận peering và cập nhật route table cả 2 VPC <br>&emsp; + Khởi tạo EC2 trong từng VPC và test ping/SSH qua peering <br>&emsp; + Xác minh Security Group cho phép traffic từ CIDR VPC peer | 23/06/2026 | 23/06/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/create-vpc-peering-connection.html> |
| 4   | - **Thực hành:** AWS Transit Gateway <br>&emsp; + Tạo Transit Gateway với ECMP và DNS support <br>&emsp; + Attach VPC-A và VPC-B vào Transit Gateway <br>&emsp; + Tạo VPC thứ ba (10.2.0.0/16) và attach vào TGW <br>&emsp; + Cấu hình TGW route table định tuyến traffic giữa 3 VPC <br>&emsp; + Test kết nối full mesh: VPC-A ↔ VPC-B ↔ VPC-C qua TGW | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/vpc/latest/tgw/> |
| 5   | - **Thực hành:** Lambda automation với EventBridge <br>&emsp; + Viết Lambda `StopDevInstances`: query EC2 theo tag (Env=dev), dừng toàn bộ <br>&emsp; + Viết Lambda `StartDevInstances`: khởi động instance dev theo tag <br>&emsp; + Tạo EventBridge Scheduled Rule: dừng lúc 20:00, khởi động lúc 08:00 ngày làm việc <br>&emsp; + Cấp quyền Lambda role: ec2:StopInstances, ec2:StartInstances, ec2:DescribeInstances (giới hạn theo tag) | 25/06/2026 | 25/06/2026 | <https://docs.aws.amazon.com/eventbridge/latest/userguide/> |
| 6   | - **Thực hành:** Lambda automation phản ứng sự kiện <br>&emsp; + Viết Lambda `CleanOldSnapshots`: xóa EBS snapshot cũ hơn 30 ngày <br>&emsp; + Trigger bằng EventBridge scheduled rule (hàng tuần) <br>&emsp; + Viết Lambda `NotifyOnBudgetAlert`: nhận từ SNS Budgets, gửi webhook Slack có định dạng <br> - Xem lại IAM least-privilege policy cho tất cả Lambda role <br> - Tài liệu hóa kiến trúc tự động hóa đầy đủ | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 10:

* Thiết lập VPC Peering giữa hai VPC với cập nhật route table và Security Group rule phù hợp.

* Triển khai Transit Gateway kết nối ba VPC, cho phép kết nối full mesh giữa tất cả.

* Tự động hóa lịch start/stop EC2 dev bằng Lambda và EventBridge — tiết kiệm chi phí từ giờ idle.

* Tự động dọn EBS snapshot cũ: Lambda xóa snapshot hơn 30 ngày theo lịch hàng tuần.

* Triển khai Lambda cảnh báo ngân sách gửi webhook Slack có định dạng khi vượt ngưỡng chi phí.

* Áp dụng IAM least-privilege policy cho tất cả Lambda execution role, giới hạn theo resource tag.