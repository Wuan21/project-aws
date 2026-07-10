---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Thực hiện kiểm thử hệ thống cuối cùng trên toàn bộ tính năng chính trong môi trường production.
* Rà soát và xác nhận các thành phần hạ tầng AWS.
* Hoàn thiện tất cả tài liệu kỹ thuật và hướng dẫn người dùng.
* Chuẩn bị bài thuyết trình cuối, demo và đề xuất cải tiến tương lai.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Lập danh sách kiểm thử cuối bao phủ tất cả tính năng cốt lõi <br> - Kiểm thử lại xác thực: đăng ký, xác minh OTP, đăng nhập, duy trì session và đăng xuất <br> - Kiểm thử lại quản lý quiz: tạo quiz, thêm câu hỏi, chỉnh sửa quiz, xóa quiz <br> - Kiểm thử lại quản lý phòng: tạo phòng, tham gia phòng bằng PIN, chuyển đổi trạng thái phòng | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Kiểm thử hệ thống cuối:** Gameplay thời gian thực <br>&emsp; + Kiểm thử luồng game đầy đủ với nhiều phiên Player đồng thời <br>&emsp; + Kiểm thử hành vi WebSocket với 5+ người chơi đồng thời: phân phối message, độ trễ và thứ tự <br>&emsp; + Kiểm thử nộp câu trả lời, cập nhật điểm và độ chính xác bảng xếp hạng dưới tải đồng thời <br>&emsp; + Xác minh trang kết quả cuối hiển thị thứ hạng và điểm số chính xác | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Rà soát hạ tầng AWS:** <br>&emsp; + Xác minh CloudFront distribution: cache behavior, HTTPS, SPA routing và response header <br>&emsp; + Xác minh S3 bucket: OAC policy, không có public access, cấu trúc file tĩnh đúng <br>&emsp; + Rà soát Cognito User Pool: thời hạn token, cài đặt MFA nếu có <br>&emsp; + Rà soát CloudWatch Dashboard: kiểm tra metrics đang ghi nhận đúng cho tất cả dịch vụ giám sát | 08/07/2026 | 08/07/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |
| 5   | - **Hoàn thiện tài liệu:** <br>&emsp; + Rà soát và hoàn thiện tài liệu kỹ thuật: kiến trúc hệ thống, thiết kế API, data model, IAM policies <br>&emsp; + Rà soát và hoàn thiện tài liệu người dùng: Hướng dẫn sử dụng, phần FAQ <br>&emsp; + Cập nhật Worklog cho cả 12 tuần <br>&emsp; + Chuẩn bị slide thuyết trình cuối: phát biểu vấn đề, kiến trúc, luồng demo, bài học chính | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Chuẩn bị cuối và nhìn lại dự án:** <br>&emsp; + Tập dượt demo cuối end-to-end trong môi trường production <br>&emsp; + Xác định và ghi lại các hạn chế còn lại của hệ thống <br>&emsp; + Đề xuất cải tiến tương lai: phân tích nâng cao, bảng xếp hạng cải tiến, thêm chế độ chơi, CI/CD pipeline <br>&emsp; + Hoàn thiện tự đánh giá và nhìn lại kỳ thực tập <br>&emsp; + Nộp báo cáo thực tập cuối và tất cả tài liệu yêu cầu | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 12:

* Hoàn thành kiểm thử hệ thống cuối trong môi trường production — tất cả tính năng cốt lõi bao gồm xác thực, quản lý quiz, quản lý phòng và gameplay thời gian thực đều hoạt động đúng.

* Kiểm thử hành vi WebSocket với nhiều người chơi đồng thời — phân phối message, cập nhật điểm và độ chính xác bảng xếp hạng được xác minh dưới tải đồng thời.

* Rà soát và xác nhận các thành phần hạ tầng AWS: CloudFront, S3, Cognito và CloudWatch được cấu hình đúng và hoạt động ổn định.

* Hoàn thiện tất cả tài liệu kỹ thuật bao gồm kiến trúc hệ thống, thiết kế API, data model và IAM policies.

* Hoàn thiện Hướng dẫn sử dụng và chuẩn bị đầy đủ slide thuyết trình cuối.

* Xác định các hạn chế còn lại của hệ thống và đề xuất cải tiến tương lai bao gồm phân tích nâng cao, bảng xếp hạng cải tiến, thêm chế độ chơi và CI/CD pipeline cho deploy tự động.

* Dự án thực tập SyncQuiz được hoàn thành thành công và toàn bộ tài liệu yêu cầu được nộp đúng hạn.
