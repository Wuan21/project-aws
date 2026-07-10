---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
### Mục tiêu tuần 3:

* Tìm hiểu về Amazon Cognito và vai trò trong xác thực người dùng.
* Tìm hiểu về Amazon API Gateway và cách xây dựng REST API trên AWS.
* Tìm hiểu về API Gateway WebSocket API cho giao tiếp thời gian thực.
* Phân tích cách áp dụng Cognito, API Gateway và WebSocket API vào dự án SyncQuiz.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu Amazon Cognito: tổng quan, mục đích và các thành phần chính <br>&emsp; + User Pool: đăng ký, đăng nhập người dùng và quản lý danh tính <br>&emsp; + App Client: cấu hình quyền truy cập cấp ứng dụng <br>&emsp; + JWT token: ID token, access token và refresh token <br> - Hiểu luồng đăng ký và đăng nhập Cognito | 04/05/2026 | 04/05/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |
| 3   | - Nghiên cứu Amazon API Gateway: tổng quan và cách xây dựng REST API trên AWS <br>&emsp; + Resource và route, HTTP method, mapping request/response <br>&emsp; + Lambda proxy integration: kết nối API Gateway với Lambda function <br>&emsp; + Authorizer: dùng Cognito JWT Authorizer để bảo vệ route API <br>&emsp; + Cấu hình CORS cho giao tiếp với frontend | 05/05/2026 | 05/05/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |
| 4   | - **Thực hành:** Kết nối API Gateway với AWS Lambda <br>&emsp; + Tạo REST API trong API Gateway <br>&emsp; + Tạo route và tích hợp với Lambda function <br>&emsp; + Thêm Cognito JWT Authorizer để bảo vệ route nhạy cảm <br>&emsp; + Kiểm thử bằng Postman hoặc API Gateway console | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Nghiên cứu API Gateway WebSocket API cho ứng dụng thời gian thực <br>&emsp; + Hiểu vòng đời kết nối WebSocket: $connect, $disconnect, $default route <br>&emsp; + Tìm hiểu cách client kết nối, gửi message và nhận broadcast message <br>&emsp; + Nghiên cứu cách Lambda xử lý WebSocket message và quản lý connection ID | 07/05/2026 | 07/05/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 6   | - Phân tích cách áp dụng Cognito, API Gateway và WebSocket API vào dự án SyncQuiz <br>&emsp; + Cognito: xác thực host và quản lý session người dùng <br>&emsp; + REST API: CRUD quiz, tạo phòng và thao tác người chơi tham gia <br>&emsp; + WebSocket API: giao tiếp game thời gian thực, danh sách người chơi và bảng xếp hạng trực tiếp <br> - Ghi chú thiết kế cho kiến trúc backend SyncQuiz | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 3:

* Tìm hiểu Amazon Cognito và hiểu User Pool, App Client và luồng xác thực dựa trên JWT token.

* Nghiên cứu Amazon API Gateway và hiểu cách xây dựng REST API tích hợp Lambda và Cognito JWT Authorizer.

* Thực hành thành công kết nối API Gateway với Lambda function và kiểm thử route được bảo vệ bằng Cognito.

* Tìm hiểu API Gateway WebSocket API và hiểu vòng đời kết nối, định tuyến message và cách Lambda xử lý message thời gian thực.

* Phân tích cách áp dụng Cognito, REST API và WebSocket API vào dự án SyncQuiz: Cognito để xác thực người dùng, REST API để quản lý quiz và phòng chơi, WebSocket API để giao tiếp gameplay thời gian thực và bảng xếp hạng trực tiếp.