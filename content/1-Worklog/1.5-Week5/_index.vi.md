---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---
### Mục tiêu tuần 5:

* Triển khai Application Load Balancer để phân phối traffic đến nhiều EC2 instance.
* Cấu hình Auto Scaling Group với chính sách mở rộng động cho tầng ứng dụng.
* Thiết lập AWS Budgets và Cost Explorer để theo dõi và kiểm soát chi phí cloud.
* Xác minh high availability qua test lỗi instance và tự động thay thế.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Elastic Load Balancing: so sánh ALB, NLB và CLB <br> - Tìm hiểu thành phần ALB: listener, rules, target group, health check <br> - Tìm hiểu Auto Scaling Group: desired/min/max capacity, chính sách scaling (target tracking, step scaling, scheduled) | 18/05/2026 | 18/05/2026 | <https://docs.aws.amazon.com/elasticloadbalancing/> |
| 3   | - **Thực hành:** Tạo Application Load Balancer <br>&emsp; + Tạo Target Group (port 3000, HTTP health check trên /health) <br>&emsp; + Tạo ALB trong public subnet, cấu hình listener port 80 <br>&emsp; + Đăng ký EC2 instance vào target group <br>&emsp; + Kiểm tra traffic cân bằng qua ALB DNS name | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Tạo Auto Scaling Group <br>&emsp; + Tạo Launch Template với user data triển khai app <br>&emsp; + Cấu hình ASG: min 2, desired 2, max 6 instance trên 2 AZ <br>&emsp; + Gắn ASG vào ALB Target Group <br>&emsp; + Thêm Target Tracking Scaling policy (ngưỡng CPU 60%) <br>&emsp; + Bật Scale-In protection cho instance mới | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/autoscaling/ec2/userguide/> |
| 5   | - **Thực hành:** AWS Budgets và Cost Management <br>&emsp; + Tạo cost budget theo tháng với cảnh báo email tại 80% và 100% <br>&emsp; + Tạo usage budget cho số giờ EC2 <br>&emsp; + Khám phá Cost Explorer: lọc theo service, tag, region <br>&emsp; + Bật Cost Allocation Tags theo dõi tài nguyên | 21/05/2026 | 21/05/2026 | <https://docs.aws.amazon.com/cost-management/> |
| 6   | - **Kiểm tra tải và khả năng phục hồi:** <br>&emsp; + Dùng Apache Bench (ab) tạo tải để trigger scale-out <br>&emsp; + Quan sát activity log ASG: instance đang được khởi tạo <br>&emsp; + Xóa instance thủ công, xác minh ASG thay thế tự động <br>&emsp; + Xác minh ALB health check loại bỏ instance không khỏe <br> - Xem lại lịch sử scaling và CloudWatch metrics | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

* Triển khai Application Load Balancer với target group, health check và listener rule.

* Tạo Auto Scaling Group với min/desired/max capacity trên 2 Availability Zone.

* Cấu hình Target Tracking scaling dựa trên CPU — scale-out trigger thành công khi có tải cao.

* Xác minh high availability: xóa instance và ASG tự động khởi tạo thay thế.

* Thiết lập AWS Budgets với cảnh báo chi phí và usage để chủ động quản lý ngân sách.

* Sử dụng Cost Explorer phân tích chi phí theo service và áp dụng cost allocation tag cho theo dõi chi tiết.