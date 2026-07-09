---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu tuần 8:

* Giám sát sức khỏe ứng dụng và hạ tầng bằng Amazon CloudWatch.
* Tạo CloudWatch Alarm cho tỷ lệ lỗi API và độ sâu hàng đợi SQS.
* Gửi cảnh báo vận hành đến quản trị viên qua SNS khi vượt ngưỡng.
* Sử dụng CloudWatch Dashboard và Log Insights để quan sát hệ thống.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu CloudWatch: Metrics, Namespace, Dimension, Statistics <br> - Tìm hiểu CloudWatch Alarms: loại ngưỡng (static, anomaly detection), evaluation period <br> - Tìm hiểu CloudWatch Logs: log group, log stream, metric filter, retention policy <br> - Xem lại các metric quan trọng: ALB 5XXCount, SQS ApproximateNumberOfMessagesNotVisible, Lambda Errors | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/cloudwatch/> |
| 3   | - **Thực hành:** Tạo CloudWatch Alarms <br>&emsp; + Alarm 1: ALB `HTTPCode_ELB_5XX_Count` > 10 trong 5 phút → trạng thái ALARM <br>&emsp; + Alarm 2: SQS `ApproximateNumberOfMessagesNotVisible` > 100 → ALARM <br>&emsp; + Alarm 3: Lambda `Errors` > 5 trong 1 phút → ALARM <br>&emsp; + Cấu hình SNS topic làm alarm action gửi email cảnh báo đến admin | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html> |
| 4   | - **Thực hành:** Xây dựng CloudWatch Dashboard <br>&emsp; + Thêm widget: Request Count ALB, 5XX errors, Target Response Time <br>&emsp; + Thêm độ sâu hàng đợi SQS và tỷ lệ lỗi/invocation Lambda <br>&emsp; + Thêm CPU RDS và số kết nối database <br>&emsp; + Cấu hình auto-refresh 1 phút <br> - Tạo metric filter CloudWatch Logs cho từ khóa lỗi ứng dụng | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html> |
| 5   | - **Thực hành:** Mô phỏng điều kiện kích hoạt alarm <br>&emsp; + Inject HTTP 500 error qua API để trigger alarm ALB 5XX <br>&emsp; + Tạm dừng Lambda consumer SQS để tin nhắn tích lũy <br>&emsp; + Xác minh email cảnh báo SNS nhận trong kỳ đánh giá alarm <br> - Dùng CloudWatch Log Insights truy vấn: `stats count(*) by errorType | sort count desc` | 11/06/2026 | 11/06/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html> |
| 6   | - Cấu hình Composite Alarm kết hợp điều kiện lỗi API + độ sâu SQS <br> - Bật CloudWatch Contributor Insights trên ALB access log <br> - Bật Container Insights cho ECS (chuẩn bị tuần 9) <br> - Xem lại và tinh chỉnh ngưỡng alarm dựa trên metric baseline <br> - Tài liệu hóa runbook giám sát và cảnh báo | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

* Cấu hình CloudWatch Alarm cho tỷ lệ lỗi 5XX ALB, độ sâu hàng đợi SQS và tỷ lệ lỗi Lambda.

* Nhận email cảnh báo SNS thành công khi ngưỡng alarm bị vi phạm trong các bài test mô phỏng.

* Xây dựng CloudWatch Dashboard đa dịch vụ theo dõi sức khỏe ứng dụng thời gian thực.

* Dùng CloudWatch Log Insights truy vấn log ứng dụng và xác định pattern lỗi hàng đầu.

* Tạo Composite Alarm kết hợp nhiều điều kiện để giảm nhiễu cảnh báo.

* Tài liệu hóa runbook xử lý sự cố khi alarm kích hoạt.