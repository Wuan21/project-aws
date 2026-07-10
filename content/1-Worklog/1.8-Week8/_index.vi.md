---
title: "Tuần 8: Host View, Player View và Waiting Room real-time"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu tuần 8:

* Phát triển giao diện Host và Player cho quản lý phòng chơi quiz.
* Tích hợp WebSocket client vào frontend để giao tiếp thời gian thực.
* Xây dựng giao diện Waiting Room với cập nhật danh sách người chơi thời gian thực.
* Kiểm thử kết nối, ngắt kết nối WebSocket và đồng bộ dữ liệu trực tiếp.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu giao thức WebSocket và browser WebSocket API <br> - Xem xét cấu trúc message và vòng đời kết nối của AWS API Gateway WebSocket API <br> - Thiết kế luồng giao tiếp thời gian thực: kết nối, tham gia phòng, broadcast danh sách người chơi, bắt đầu game | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 3   | - **Thực hành:** Phát triển giao diện Host tạo phòng chơi <br>&emsp; + Tạo trang Host: chọn quiz, tạo mã PIN phòng, hiển thị mã phòng cho người chơi <br>&emsp; + Kết nối Host với WebSocket khi tạo phòng <br>&emsp; + Hiển thị waiting room: cập nhật danh sách người chơi thời gian thực <br>&emsp; + Thêm nút Start Game gửi tín hiệu bắt đầu game qua WebSocket | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Phát triển giao diện Player tham gia phòng <br>&emsp; + Tạo trang Join Room: nhập mã phòng và biệt danh người chơi <br>&emsp; + Kết nối Player với WebSocket sau khi gửi mã phòng <br>&emsp; + Hiển thị Waiting Room UI: mã phòng, thông báo chờ và số người chơi <br>&emsp; + Xử lý xác nhận tham gia và thông báo lỗi (phòng không tồn tại, phòng đã đầy) | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Thực hành:** Tích hợp WebSocket client vào core frontend <br>&emsp; + Tạo module WebSocket service tập trung (connect, disconnect, send, onMessage) <br>&emsp; + Xử lý logic kết nối lại khi mất kết nối <br>&emsp; + Phân tích message WebSocket đến theo loại action và dispatch vào state <br>&emsp; + Cập nhật danh sách người chơi thời gian thực khi có người tham gia hoặc rời phòng | 11/06/2026 | 11/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/websocket-api-develop-routes.html> |
| 6   | - Kiểm thử thiết lập kết nối WebSocket và xử lý ngắt kết nối <br> - Xác minh cập nhật danh sách người chơi thời gian thực trong giao diện Host và Player <br> - Mô phỏng gián đoạn mạng và kiểm thử hành vi kết nối lại <br> - Xem xét và sửa các race condition hoặc vấn đề về thứ tự message | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

* Phát triển giao diện Host cho tạo phòng chơi, hiển thị mã PIN phòng và quản lý waiting room thời gian thực.

* Phát triển giao diện Player với luồng nhập mã phòng và Waiting Room UI hiển thị thông tin người chơi trực tiếp.

* Tích hợp module WebSocket client tập trung vào frontend để xử lý message nhất quán trên toàn bộ component.

* Triển khai cập nhật danh sách người chơi thời gian thực trong Waiting Room bằng WebSocket push message.

* Kiểm thử thành công thiết lập kết nối WebSocket, xử lý ngắt kết nối và hành vi kết nối lại.

* Hệ thống sẵn sàng hỗ trợ gameplay thời gian thực trong tuần tiếp theo.