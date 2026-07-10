---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
### Mục tiêu tuần 6:

* Khởi tạo boilerplate dự án React frontend cho SyncQuiz.
* Cấu hình hệ thống routing và quản lý state cho ứng dụng.
* Tạo các component UI tái sử dụng để hỗ trợ phát triển tính năng về sau.
* Chuẩn hóa cấu trúc dự án để đảm bảo khả năng mở rộng và bảo trì.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Nghiên cứu các thực hành tốt nhất khi thiết lập dự án React <br> - Khởi tạo dự án React frontend bằng Create React App hoặc Vite <br> - Cấu hình ESLint, Prettier và các tiêu chuẩn code | 25/05/2026 | 25/05/2026 | <https://vitejs.dev/guide/> |
| 3   | - **Thực hành:** Cấu hình hệ thống routing <br>&emsp; + Cài đặt và thiết lập React Router v6 <br>&emsp; + Định nghĩa cấu trúc route: Home, Login, Signup, Dashboard, Quiz Management, Game Room <br>&emsp; + Triển khai protected routes cho người dùng đã xác thực <br>&emsp; + Thiết lập navigation guard dựa trên trạng thái xác thực | 26/05/2026 | 26/05/2026 | <https://reactrouter.com/en/main> |
| 4   | - **Thực hành:** Thiết lập quản lý state <br>&emsp; + Đánh giá và lựa chọn giải pháp quản lý state (Redux Toolkit / Zustand / Context API) <br>&emsp; + Triển khai global auth state: thông tin người dùng, token, trạng thái đăng nhập <br>&emsp; + Triển khai UI state: loading indicator, modal, thông báo lỗi <br>&emsp; + Viết unit test cho state reducer hoặc context provider | 27/05/2026 | 27/05/2026 | <https://redux-toolkit.js.org/> |
| 5   | - **Thực hành:** Xây dựng component base tái sử dụng <br>&emsp; + Tạo component Header với navigation và thông tin người dùng <br>&emsp; + Tạo component Footer <br>&emsp; + Tạo Layout wrapper component cho cấu trúc trang nhất quán <br>&emsp; + Tạo Loading spinner và Error Boundary component <br>&emsp; + Áp dụng CSS/Tailwind cơ bản để đảm bảo giao diện thống nhất | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Chuẩn hóa cấu trúc thư mục: components/, pages/, hooks/, store/, services/, utils/ <br> - Xác minh dự án chạy đúng trong môi trường phát triển cục bộ <br> - Thiết lập biến môi trường (.env) cho API endpoint và cấu hình <br> - Ghi lại tài liệu về cấu trúc dự án và hướng dẫn sử dụng component | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 6:

* Khởi tạo thành công dự án React frontend với Vite, ESLint và Prettier.

* Cấu hình React Router v6 với cấu trúc route đầy đủ, bao gồm protected routes cho các trang yêu cầu xác thực.

* Triển khai quản lý state toàn cục cho xác thực và UI state.

* Xây dựng các component base tái sử dụng: Header, Footer, Layout, Loading và Error Boundary.

* Thiết lập cấu trúc thư mục chuẩn hóa để hỗ trợ phát triển có khả năng mở rộng trong các tuần tiếp theo.

* Dự án chạy đúng trong môi trường phát triển cục bộ với cấu hình biến môi trường sẵn sàng.