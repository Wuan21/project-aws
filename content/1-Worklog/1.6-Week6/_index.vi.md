---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
### Mục tiêu tuần 6:

* Thiết kế hệ thống gamification tương tác người dùng bằng serverless AWS.
* Triển khai logic tính điểm với AWS Lambda và lưu trữ bảng xếp hạng bằng DynamoDB.
* Expose chức năng bảng xếp hạng qua Amazon API Gateway.
* Kiểm tra luồng tính điểm và xếp hạng end-to-end.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu DynamoDB: table, partition key, sort key, GSI, LSI <br> - Tìm hiểu Lambda: mô hình thực thi, trigger, biến môi trường, layer <br> - Thiết kế data model gamification: điểm người dùng, thành tích, thứ hạng bảng xếp hạng | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 3   | - **Thực hành:** Thiết lập bảng xếp hạng DynamoDB <br>&emsp; + Tạo bảng `leaderboard` (partition key: userId, sort key: timestamp) <br>&emsp; + Tạo GSI trên thuộc tính `score` cho truy vấn xếp hạng <br>&emsp; + Viết Lambda `submitScore`: xác thực input, ghi item vào DynamoDB <br>&emsp; + Test Lambda cục bộ bằng SAM CLI | 26/05/2026 | 26/05/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/> |
| 4   | - **Thực hành:** Xây dựng Lambda truy vấn bảng xếp hạng <br>&emsp; + Viết Lambda `getLeaderboard`: truy vấn DynamoDB GSI theo điểm giảm dần <br>&emsp; + Thêm hỗ trợ phân trang (Limit + ExclusiveStartKey) <br>&emsp; + Tạo API Gateway REST API với resource `/score` (POST) và `/leaderboard` (GET) <br>&emsp; + Cấu hình Lambda proxy integration cho từng route | 27/05/2026 | 27/05/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |
| 5   | - Tích hợp API Gateway vào frontend Node.js <br>&emsp; + Thêm xác thực API key cho API Gateway <br>&emsp; + Cập nhật cài đặt CORS cho phép origin frontend <br>&emsp; + Deploy API lên stage `prod` <br> - Test luồng đầy đủ: submit điểm → DynamoDB → truy vấn API bảng xếp hạng | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Thêm hệ thống thành tích: Lambda kiểm tra mốc (top 10) ghi vào bảng `achievements` <br> - Cấu hình DynamoDB Streams kích hoạt Lambda thành tích khi có điểm mới <br> - Load test: submit 100 điểm đồng thời, xác minh tính nhất quán DynamoDB và API <br> - Xem xét cold start Lambda và tối ưu bằng Provisioned Concurrency | 29/05/2026 | 29/05/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html> |


### Kết quả đạt được tuần 6:

* Thiết kế và triển khai hệ thống gamification serverless với Lambda, DynamoDB và API Gateway.

* Tạo bảng DynamoDB với Global Secondary Index cho truy vấn bảng xếp hạng hiệu quả theo điểm số.

* Phát triển và deploy Lambda function xử lý nộp điểm và truy vấn bảng xếp hạng.

* Expose API bảng xếp hạng qua API Gateway với xác thực API key và cấu hình CORS.

* Triển khai DynamoDB Streams kích hoạt kiểm tra thành tích khi có điểm mới.

* Load test với 100 submission đồng thời — toàn bộ bản ghi nhất quán.