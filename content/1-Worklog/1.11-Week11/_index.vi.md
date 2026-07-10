---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Thực hiện kiểm thử người dùng và kiểm thử responsive trong môi trường production.
* Xác định và sửa các lỗi UI/UX và vấn đề logic frontend.
* Cải thiện độ ổn định của component và trải nghiệm người dùng tổng thể.
* Chuẩn bị Hướng dẫn sử dụng và kịch bản demo cho bài thuyết trình cuối.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Lập kế hoạch phạm vi kiểm thử: tính năng, thiết bị, trình duyệt và vai trò người dùng (Host, Player) <br> - Chuẩn bị test case: đăng ký, đăng nhập, tạo quiz, tạo phòng, tham gia phòng, gameplay, bảng xếp hạng và kết quả <br> - Chuẩn bị thiết bị kiểm thử: máy tính, tablet và điện thoại | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Kiểm thử production:** Luồng người dùng Host <br>&emsp; + Kiểm thử đăng ký → đăng nhập → tạo quiz → tạo phòng → bắt đầu game → điều khiển câu hỏi → kết thúc game <br>&emsp; + Xác minh Host có thể điều khiển luồng game không có lỗi <br>&emsp; + Kiểm thử responsive trên máy tính và tablet <br>&emsp; + Ghi lại tất cả lỗi và hành vi bất thường phát hiện trong kiểm thử | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Kiểm thử production:** Luồng người dùng Player <br>&emsp; + Kiểm thử tham gia phòng → waiting room → gameplay → nộp câu trả lời → bảng xếp hạng → kết quả <br>&emsp; + Kiểm thử với nhiều phiên Player đồng thời <br>&emsp; + Kiểm thử responsive trên thiết bị di động <br>&emsp; + Kiểm thử hành vi kết nối lại WebSocket khi mất kết nối giữa game | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Sửa lỗi và cải thiện UX:** <br>&emsp; + Sửa lỗi căn chỉnh UI và layout trên màn hình nhỏ <br>&emsp; + Sửa lỗi logic frontend: các trường hợp biên của nộp câu trả lời, vấn đề đồng bộ timer <br>&emsp; + Cải thiện thông báo lỗi để hướng dẫn người dùng tốt hơn <br>&emsp; + Cải thiện trạng thái loading và chuyển đổi giữa các giai đoạn game <br>&emsp; + Xác minh tất cả bản sửa lỗi trong môi trường production sau khi deploy | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Chuẩn bị tài liệu:** <br>&emsp; + Viết Hướng dẫn sử dụng: mô tả cách đăng ký, tạo quiz, host game và tham gia với vai trò Player <br>&emsp; + Thêm ảnh chụp màn hình vào Hướng dẫn cho từng bước chính <br>&emsp; + Chuẩn bị kịch bản demo: xác định luồng và các điểm trình bày cho stakeholder <br>&emsp; + Rà soát tài liệu về độ rõ ràng, chính xác và đầy đủ | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 11:

* Thực hiện kiểm thử người dùng toàn diện trong môi trường production bao phủ luồng Host và Player.

* Kiểm thử responsive trên máy tính, tablet và điện thoại — các vấn đề được xác định và sửa chữa.

* Sửa các lỗi UI/UX bao gồm lỗi căn chỉnh layout, không nhất quán thông báo lỗi và thiếu trạng thái loading.

* Sửa lỗi logic frontend liên quan đến các trường hợp biên của nộp câu trả lời và đồng bộ timer.

* Cải thiện độ ổn định component và trải nghiệm người dùng trên tất cả giai đoạn game chính.

* Hoàn thành Hướng dẫn sử dụng kèm ảnh chụp màn hình và chuẩn bị kịch bản demo cho bài thuyết trình cuối.
