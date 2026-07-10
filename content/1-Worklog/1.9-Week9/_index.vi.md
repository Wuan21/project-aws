---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:

* Phát triển trang gameplay của Host với chức năng điều khiển câu hỏi.
* Phát triển trang gameplay của Player với chức năng nộp câu trả lời.
* Tích hợp bảng xếp hạng thời gian thực và cập nhật điểm trong gameplay.
* Xây dựng trang Kết quả Game và kiểm thử toàn bộ luồng game.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Thiết kế state machine gameplay: waiting → in-progress → question → answer → leaderboard → ended <br> - Lập kế hoạch các loại WebSocket message cho gameplay: startGame, showQuestion, submitAnswer, showLeaderboard, endGame <br> - Thiết kế wireframe trang gameplay cho Host và Player | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Thực hành:** Phát triển trang gameplay Host <br>&emsp; + Hiển thị số câu hỏi hiện tại, nội dung câu hỏi và các đáp án <br>&emsp; + Hiển thị đồng hồ đếm ngược cho mỗi câu hỏi <br>&emsp; + Triển khai nút Next Question: gửi action WebSocket để chuyển câu tiếp theo <br>&emsp; + Hiển thị tiến độ nộp câu trả lời (số người chơi đã trả lời) <br>&emsp; + Xử lý action End Game và chuyển sang trang kết quả | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Phát triển trang gameplay Player <br>&emsp; + Hiển thị câu hỏi và các đáp án nhận qua WebSocket <br>&emsp; + Triển khai chọn đáp án: highlight đáp án được chọn, vô hiệu hóa chọn lại sau khi nộp <br>&emsp; + Gửi đáp án đã chọn lên backend qua WebSocket khi chọn <br>&emsp; + Hiển thị phản hồi sau khi nộp câu trả lời (chờ câu tiếp theo) <br>&emsp; + Xử lý chuyển đổi trạng thái game: câu hỏi → chờ → câu tiếp theo → game kết thúc | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Thực hành:** Tích hợp bảng xếp hạng thời gian thực <br>&emsp; + Hiển thị bảng xếp hạng giữa các câu hỏi: hạng, tên người chơi, điểm hiện tại <br>&emsp; + Cập nhật điểm thời gian thực khi backend broadcast sự kiện cập nhật điểm <br>&emsp; + Thêm animation thay đổi hạng trên bảng xếp hạng <br>&emsp; + Xử lý logic hiển thị khi có người chơi điểm bằng nhau | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** Phát triển trang Kết quả Game <br>&emsp; + Hiển thị bảng xếp hạng chung cuộc: top 3 và danh sách đầy đủ người chơi với điểm cuối <br>&emsp; + Cung cấp tùy chọn quay về Dashboard hoặc bắt đầu game mới <br>&emsp; + Kiểm thử toàn bộ luồng game: tạo phòng → người chơi tham gia → bắt đầu game → trả lời → bảng xếp hạng → kết quả <br>&emsp; + Sửa các vấn đề phát hiện trong kiểm thử end-to-end | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

* Phát triển trang gameplay Host với điều khiển câu hỏi đầy đủ, đồng hồ đếm ngược và theo dõi tiến độ trả lời.

* Phát triển trang gameplay Player với chọn đáp án, phản hồi thời gian thực và chuyển đổi trạng thái mượt mà.

* Tích hợp bảng xếp hạng thời gian thực cập nhật điểm động sau mỗi câu hỏi qua WebSocket event.

* Xây dựng trang Kết quả Game hiển thị bảng xếp hạng đầy đủ và điểm cuối cho tất cả người chơi.

* Hoàn thành kiểm thử end-to-end toàn bộ luồng game từ tạo phòng đến hiển thị kết quả cuối.

* Trải nghiệm gameplay cốt lõi của SyncQuiz hoạt động đầy đủ trên frontend.