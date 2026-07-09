---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Mục tiêu tuần 7:

* Hiểu Amazon SNS và SQS — dịch vụ nhắn tin và thông báo.
* Tích hợp SNS gửi thông báo thời gian thực khi có sự kiện ứng dụng.
* Xây dựng mô hình fanout thông báo tin cậy qua SNS và SQS.
* Kiểm tra việc giao thông báo qua nhiều loại subscription.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Amazon SNS: topic, subscription (email, SMS, HTTP/S, Lambda, SQS), message filtering <br> - Tìm hiểu Amazon SQS: standard queue vs FIFO, visibility timeout, dead-letter queue <br> - Tìm hiểu fanout pattern SNS + SQS cho giao thông báo tách rời | 01/06/2026 | 01/06/2026 | <https://docs.aws.amazon.com/sns/latest/dg/> |
| 3   | - **Thực hành:** Tạo SNS topic và subscription <br>&emsp; + Tạo SNS Standard topic `AppNotifications` <br>&emsp; + Thêm email subscription và xác nhận qua hộp thư <br>&emsp; + Thêm SMS subscription (số E.164) <br>&emsp; + Publish test message và xác minh giao đến tất cả subscriber <br>&emsp; + Cấu hình message filter policy cho từng subscription | 02/06/2026 | 02/06/2026 | <https://docs.aws.amazon.com/sns/latest/dg/sns-getting-started.html> |
| 4   | - **Thực hành:** Tích hợp SNS vào ứng dụng <br>&emsp; + Thêm AWS SDK v3 SNS client vào Node.js app <br>&emsp; + Publish SNS message khi có sự kiện: điểm cao mới, mở khóa thành tích <br>&emsp; + Đính kèm message attribute (userId, eventType, score) <br>&emsp; + Viết Lambda subscriber xử lý sự kiện SNS và log vào CloudWatch | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Thực hành:** Xây dựng SQS buffer xử lý bất đồng bộ <br>&emsp; + Tạo SQS Standard queue `ScoreQueue` và subscribe vào SNS topic <br>&emsp; + Tạo Dead Letter Queue cho message lỗi (maxReceiveCount: 3) <br>&emsp; + Cấu hình Lambda poll SQS queue (event source mapping) <br>&emsp; + Test: publish SNS → SQS giao đến Lambda → Lambda xử lý và log | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| 6   | - Test kịch bản lỗi: <br>&emsp; + Mô phỏng Lambda xử lý lỗi → message chuyển DLQ sau 3 lần thử lại <br>&emsp; + Test SQS visibility timeout với consumer chậm <br>&emsp; + Xác minh DLQ message inspection và re-drive policy <br> - Đo độ trễ giao thông báo SNS (email, SMS, Lambda) <br> - Tài liệu hóa kiến trúc thông báo | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

* Tạo và cấu hình SNS topic với nhiều loại subscription: email, SMS và SQS.

* Giao thông báo SNS thành công khi có sự kiện ứng dụng (điểm cao mới, mở khóa thành tích).

* Triển khai message filter policy điều hướng loại sự kiện cụ thể đến subscriber đúng.

* Xây dựng SQS fanout buffer với Dead Letter Queue xử lý lỗi hiệu quả.

* Cấu hình Lambda event source mapping xử lý SQS message bất đồng bộ.

* Test DLQ: message chuyển đúng sau 3 lần xử lý thất bại.