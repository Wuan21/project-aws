---
title: "Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
menuTitle: "Tuần 5"
linkTitle: "Tuần 5"
---
### Mục tiêu tuần 5:

* Thực hành kết hợp các dịch vụ AWS đã học trong các tuần trước.
* Đánh giá cách tích hợp các dịch vụ AWS trong kiến trúc SyncQuiz.
* Thử nghiệm WebSocket API cho các tính năng giao tiếp thời gian thực.
* Chuẩn bị ý tưởng kiến trúc ban đầu cho hệ thống quiz thời gian thực SyncQuiz.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Ôn tập và củng cố kiến thức tất cả dịch vụ AWS đã học từ Tuần 1 đến Tuần 4 <br> - Xây dựng luồng backend serverless cơ bản bằng Lambda và API Gateway <br>&emsp; + Tạo nhiều Lambda function cho các nghiệp vụ khác nhau <br>&emsp; + Tạo API Gateway route và tích hợp từng route với Lambda function tương ứng <br>&emsp; + Kiểm thử end-to-end: gửi HTTP request → API Gateway → Lambda → trả về response | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Cấu hình Cognito để quản lý xác thực người dùng <br>&emsp; + Tạo Cognito User Pool với đăng nhập bằng email <br>&emsp; + Tạo App Client và cấu hình cài đặt token <br>&emsp; + Kiểm thử luồng đăng ký và đăng nhập bằng Cognito console <br>&emsp; + Kiểm thử cách dịch vụ frontend/backend dùng Cognito token để gọi API được bảo vệ | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Thử nghiệm WebSocket API cho tính năng thời gian thực <br>&emsp; + Tạo WebSocket API trong API Gateway với $connect, $disconnect và $default route <br>&emsp; + Tạo Lambda function xử lý từng WebSocket route <br>&emsp; + Kiểm thử kết nối WebSocket bằng công cụ WebSocket client <br>&emsp; + Gửi message và xác minh Lambda nhận và phản hồi WebSocket event | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 5   | - Giám sát log và lỗi bằng CloudWatch <br>&emsp; + Xem CloudWatch Logs cho Lambda function được gọi trong kiểm thử tích hợp <br>&emsp; + Xác định và giải quyết lỗi phát hiện trong kiểm thử <br>&emsp; + Xem CloudWatch Metrics cho số request API Gateway và tỷ lệ lỗi Lambda <br>&emsp; + Thêm câu lệnh log vào Lambda để cải thiện khả năng quan sát | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Đánh giá cách kết hợp dịch vụ AWS trong kiến trúc SyncQuiz <br>&emsp; + Ánh xạ từng tính năng SyncQuiz với dịch vụ AWS phù hợp <br>&emsp; + Phác thảo sơ đồ kiến trúc high-level ban đầu cho SyncQuiz <br>&emsp; + Xác định các câu hỏi kỹ thuật và thách thức cần giải quyết trong giai đoạn dự án <br>&emsp; + Chuẩn bị ý tưởng kiến trúc ban đầu và trình bày dưới dạng SyncQuiz Project Proposal | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

* Thực hành tích hợp các dịch vụ AWS đã học trong các tuần trước để hiểu rõ hơn cách chúng hoạt động trong hệ thống thực tế.

* Xây dựng luồng backend serverless cơ bản bằng Lambda và API Gateway, kiểm thử thành công định tuyến HTTP request đến Lambda function.

* Cấu hình Cognito User Pool và App Client, kiểm thử luồng đăng ký và đăng nhập, xác minh cách Cognito token bảo vệ API route.

* Thử nghiệm API Gateway WebSocket API, tạo kết nối WebSocket hoạt động và xác minh Lambda xử lý đúng WebSocket message.

* Giám sát hành vi Lambda và API Gateway bằng CloudWatch Logs và CloudWatch Metrics, xác định và giải quyết lỗi trong kiểm thử tích hợp.

* Đánh giá cách áp dụng Cognito, API Gateway, Lambda, WebSocket API và CloudWatch vào dự án SyncQuiz, và chuẩn bị ý tưởng kiến trúc ban đầu cho hệ thống quiz thời gian thực.