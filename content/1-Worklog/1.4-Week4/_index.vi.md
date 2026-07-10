---
title: "Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
menuTitle: "Tuần 4"
linkTitle: "Tuần 4"
---
### Mục tiêu tuần 4:

* Tìm hiểu về Amazon CloudWatch để giám sát log, metrics và trạng thái hệ thống.
* Tìm hiểu về Amazon SQS và cơ chế hàng đợi tin nhắn.
* Tìm hiểu về Amazon SNS và mô hình publish/subscribe.
* So sánh vai trò của SQS và SNS trong kiến trúc hệ thống phân tán.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu Amazon CloudWatch: tổng quan và tính năng cốt lõi <br>&emsp; + CloudWatch Logs: xem và lọc log stream từ Lambda và các dịch vụ khác <br>&emsp; + CloudWatch Metrics: giám sát metric dịch vụ như Lambda invocations, errors và duration <br>&emsp; + CloudWatch Alarms: đặt cảnh báo dựa trên ngưỡng để thông báo tự động | 11/05/2026 | 11/05/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |
| 3   | - **Thực hành:** Xem Lambda logs và tạo CloudWatch Dashboard <br>&emsp; + Trigger Lambda function và xem log thực thi trong CloudWatch Logs <br>&emsp; + Khám phá Log Group và Log Stream của Lambda function <br>&emsp; + Tạo CloudWatch Dashboard cơ bản với widget cho Lambda metrics <br>&emsp; + Thêm alarm cho số lần lỗi Lambda | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Nghiên cứu Amazon SQS và cơ chế hàng đợi tin nhắn <br>&emsp; + SQS Standard Queue so với FIFO Queue: khác biệt về thứ tự và đảm bảo phân phối <br>&emsp; + Visibility timeout: ngăn xử lý trùng lặp message đang trong xử lý <br>&emsp; + Dead Letter Queue (DLQ): xử lý message thất bại sau số lần thử tối đa <br>&emsp; + Long polling: giảm API call trống khi hàng đợi rảnh | 13/05/2026 | 13/05/2026 | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| 5   | - **Thực hành:** Tạo SQS queue và kiểm thử gửi/nhận message <br>&emsp; + Tạo SQS Standard Queue <br>&emsp; + Gửi message bằng AWS Console và AWS CLI <br>&emsp; + Nhận và xóa message thủ công <br>&emsp; + Tạo Dead Letter Queue và cấu hình redrive policy (maxReceiveCount: 3) | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Nghiên cứu Amazon SNS và mô hình publish/subscribe <br>&emsp; + Topic và subscription: email, SMS, HTTP/S, Lambda và SQS <br>&emsp; + Message filter policy: định tuyến message đến subscriber cụ thể <br> - **Thực hành:** Tạo topic và gửi thông báo qua SNS <br>&emsp; + Tạo SNS Standard Topic <br>&emsp; + Thêm email subscription và xác nhận <br>&emsp; + Publish test message và xác minh phân phối <br> - So sánh SQS và SNS: mục đích, mô hình phân phối và vai trò trong hệ thống phân tán | 15/05/2026 | 15/05/2026 | <https://docs.aws.amazon.com/sns/latest/dg/> |


### Kết quả đạt được tuần 4:

* Tìm hiểu Amazon CloudWatch và hiểu cách giám sát log và metrics cho các dịch vụ AWS như Lambda qua CloudWatch Logs và CloudWatch Metrics.

* Thực hành thành công xem Lambda execution log trong CloudWatch và tạo CloudWatch Dashboard cơ bản với alarm giám sát lỗi Lambda.

* Nghiên cứu Amazon SQS và hiểu Standard Queue so với FIFO Queue, visibility timeout, Dead Letter Queue và long polling.

* Thực hành tạo SQS queue, gửi và nhận message bằng AWS Console và CLI, cấu hình Dead Letter Queue với redrive policy.

* Tìm hiểu Amazon SNS và mô hình publish/subscribe, thực hành tạo SNS topic với email subscription và xác minh phân phối thông báo.

* So sánh SQS và SNS, hiểu vai trò phù hợp của từng dịch vụ trong xử lý message bất đồng bộ và phân phối thông báo trong kiến trúc hệ thống phân tán.