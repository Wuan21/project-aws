---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Triển khai ứng dụng frontend Next.js (giao diện quản trò và người chơi) lên AWS Amplify và cấu hình CI/CD tự động dựa trên Git.
* Tích hợp Amazon Cognito User Pool để xác thực tài khoản quản trò (host/giáo viên) và quản lý phiên kết nối của người chơi.
* Triển khai và tự động hóa pipeline CI/CD cho backend WebSocket API (API Gateway WebSocket) và các Lambda handler xử lý sự kiện thời gian thực (Join Room, Submit Answer, Get Leaderboard) bằng GitHub Actions.
* Thiết lập hệ thống giám sát thời gian thực bằng CloudWatch Dashboards để theo dõi số lượng kết nối WebSocket đồng thời, độ trễ và tỷ lệ lỗi của các hàm Lambda.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu và cấu hình AWS Amplify Hosting cho ứng dụng Next.js của SyncQuizz <br> - Tích hợp với repository GitHub để tự động kích hoạt build khi push commit mới lên nhánh `main` <br> - Tùy chỉnh tệp cấu hình build `amplify.yml` để tối ưu cài đặt dependencies, build ứng dụng và lưu cache | 29/06/2026 | 29/06/2026 | <https://docs.aws.amazon.com/amplify/> |
| 3 | - Thiết lập Amazon Cognito User Pool và Client để tích hợp xác thực đăng nhập/đăng ký cho tài khoản Quản trò (Host/Teacher) <br> - Thiết kế workflow CI/CD sử dụng GitHub Actions (kết hợp Serverless Framework hoặc AWS SAM) để đóng gói và triển khai backend Serverless <br> - Cấu hình AWS credentials bảo mật trong GitHub Secrets | 30/06/2026 | 30/06/2026 | <https://docs.aws.amazon.com/cognito/> |
| 4 | - Thực hành chạy pipeline deploy toàn bộ hệ thống SyncQuizz: Frontend Next.js trên Amplify và API Gateway WebSocket/REST API backend <br> - Liên kết các biến môi trường (WebSocket URL, Cognito User Pool ID) vào ứng dụng Frontend <br> - Cấu hình CORS trên REST API và API Gateway để chấp nhận domain của frontend | 01/07/2026 | 01/07/2026 | <https://docs.github.com/en/actions/> |
| 5 | - Xây dựng CloudWatch Dashboard giám sát hoạt động của SyncQuizz: theo dõi số kết nối WebSocket đồng thời (`ConnectCount`), số lượng tin nhắn, và tài nguyên sử dụng <br> - Đo lường các chỉ số của Lambda handler: tần suất gọi hàm (Invocations), tỷ lệ lỗi (Errors) và thời gian thực thi (Duration) <br> - Cấu hình CloudWatch Metrics cho DynamoDB tables để kiểm tra năng lực đáp ứng khi người chơi gửi đáp án đồng thời | 02/07/2026 | 02/07/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |
| 6 | - Tiến hành kiểm thử tích hợp toàn trình (end-to-end): giả lập Host tạo phòng đấu, người chơi kết nối WebSocket, trả lời câu hỏi và cập nhật bảng xếp hạng thời gian thực <br> - Chạy thử nghiệm chịu tải nhẹ (giả lập 50-100 client kết nối đồng thời) và quan sát hiệu năng hệ thống trên CloudWatch Dashboard <br> - Hoàn thiện tài liệu kiến trúc, sơ đồ luồng dữ liệu WebSocket và hướng dẫn vận hành | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 11:

* Triển khai thành công Frontend Next.js của SyncQuizz lên AWS Amplify với luồng CI/CD tự động kích hoạt từ GitHub mỗi khi cập nhật code.

* Tích hợp Amazon Cognito giúp xác thực và quản lý tài khoản Quản trò an toàn, hỗ trợ quản lý phiên kết nối của người chơi một cách tin cậy.

* Tự động hóa quy trình deploy hạ tầng backend (API Gateway WebSocket, Lambda, DynamoDB) thông qua GitHub Actions pipeline nhanh chóng và nhất quán.

* Thiết kế bảng điều khiển CloudWatch Dashboard trực quan, cho phép theo dõi thời gian thực số lượng người chơi đang kết nối WebSocket, hiệu năng của Lambda và trạng thái cơ sở dữ liệu.

* Chạy thử nghiệm thành công kịch bản game thực tế, dữ liệu câu hỏi và câu trả lời đồng bộ tức thời giữa màn hình của Host và thiết bị của người chơi với độ trễ cực thấp.



