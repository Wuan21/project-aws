---
title: "Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
menuTitle: "Tuần 7"
linkTitle: "Tuần 7"
---
### Mục tiêu tuần 7:

* Phát triển trang Login và Signup tích hợp với Amazon Cognito.
* Xây dựng giao diện Dashboard người dùng và quản lý quiz.
* Đảm bảo quản lý session an toàn bằng Cognito token.
* Kiểm thử toàn bộ luồng xác thực end-to-end.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu tích hợp Amazon Cognito SDK với React <br> - Xem xét Cognito hosted UI so với custom UI <br> - Lập kế hoạch luồng xác thực: đăng ký, đăng nhập, lưu token, đăng xuất, duy trì session | 01/06/2026 | 01/06/2026 | <https://docs.amplify.aws/react/build-a-backend/auth/> |
| 3   | - **Thực hành:** Phát triển trang Login và Signup <br>&emsp; + Tạo form Signup: email, mật khẩu, xác nhận mật khẩu <br>&emsp; + Tích hợp Cognito SDK: signUp, confirmSignUp (xác minh OTP) <br>&emsp; + Tạo form Login: email và mật khẩu <br>&emsp; + Tích hợp Cognito SDK: signIn, xử lý auth token <br>&emsp; + Lưu JWT token an toàn (localStorage / chiến lược httpOnly cookie) | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Quản lý session và bảo vệ route <br>&emsp; + Triển khai tự động làm mới token bằng Cognito SDK <br>&emsp; + Xử lý session hết hạn và chuyển hướng về Login <br>&emsp; + Triển khai đăng xuất: xóa token và chuyển hướng <br>&emsp; + Bảo vệ toàn bộ route xác thực bằng global auth state <br>&emsp; + Kiểm thử duy trì đăng nhập sau khi làm mới trang | 03/06/2026 | 03/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |
| 5   | - **Thực hành:** Phát triển giao diện Dashboard <br>&emsp; + Hiển thị thông tin hồ sơ người dùng (email, tên đăng nhập) <br>&emsp; + Hiển thị lịch sử quiz: danh sách quiz do người dùng tạo <br>&emsp; + Thêm điều hướng đến tạo quiz và tạo phòng chơi <br>&emsp; + Triển khai layout responsive cho trang Dashboard | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** Phát triển giao diện quản lý quiz <br>&emsp; + Tạo form tạo quiz mới: tiêu đề, mô tả, danh mục <br>&emsp; + Tạo form thêm câu hỏi: nội dung câu hỏi, các đáp án, đáp án đúng, giới hạn thời gian <br>&emsp; + Triển khai danh sách quiz với chức năng chỉnh sửa và xóa <br>&emsp; + Kết nối form quản lý quiz với các endpoint HTTP API <br>&emsp; + Kiểm thử end-to-end: tạo quiz → thêm câu hỏi → xem trên Dashboard | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

* Phát triển đầy đủ trang Login và Signup với tích hợp Cognito SDK hoạt động ổn định.

* Triển khai quản lý session an toàn: JWT token được lưu trữ và tự động làm mới qua Cognito.

* Session được duy trì đúng sau khi làm mới trang; session hết hạn tự động chuyển hướng về trang Login.

* Xây dựng Dashboard người dùng hiển thị thông tin hồ sơ và danh sách quiz.

* Phát triển giao diện quản lý quiz cho phép tạo, chỉnh sửa và xóa quiz cùng câu hỏi.

* Luồng xác thực và chuyển hướng trang được kiểm thử thành công end-to-end.