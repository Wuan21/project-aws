---
title: "Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
menuTitle: "Tuần 10"
linkTitle: "Tuần 10"
---

### Mục tiêu tuần 10:

* Build và tối ưu hóa production bundle frontend.
* Deploy frontend lên Amazon S3 với phân phối CloudFront.
* Cấu hình Origin Access Control và bucket policy để phân phối an toàn.
* Thiết lập CloudWatch Dashboard để giám sát hệ thống.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Xem xét yêu cầu production build cho React frontend <br> - Nghiên cứu cấu hình static website hosting của Amazon S3 <br> - Nghiên cứu Amazon CloudFront: distribution, origin, behavior, caching, HTTPS và trang lỗi | 22/06/2026 | 22/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| 3   | - **Thực hành:** Build và tối ưu production bundle <br>&emsp; + Chạy production build (npm run build / vite build) <br>&emsp; + Phân tích kích thước bundle và xác định dependency lớn <br>&emsp; + Áp dụng code splitting và lazy loading theo route <br>&emsp; + Minify JavaScript và CSS, bật cài đặt nén gzip/brotli <br>&emsp; + Kiểm tra output build: index.html, assets/, cấu trúc file đúng | 23/06/2026 | 23/06/2026 | <https://vitejs.dev/guide/build.html> |
| 4   | - **Thực hành:** Deploy frontend lên Amazon S3 <br>&emsp; + Tạo S3 bucket theo quy tắc đặt tên dự án <br>&emsp; + Tắt public access block (để cho phép CloudFront truy cập qua OAC) <br>&emsp; + Upload các file production build lên S3 bucket <br>&emsp; + Xác minh file upload đúng và có thể truy cập nội bộ | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| 5   | - **Thực hành:** Cấu hình CloudFront Distribution <br>&emsp; + Tạo CloudFront distribution với S3 origin <br>&emsp; + Cấu hình Origin Access Control (OAC) và cập nhật S3 bucket policy <br>&emsp; + Đặt default root object là index.html <br>&emsp; + Cấu hình custom error response: 403/404 → /index.html (hỗ trợ SPA routing) <br>&emsp; + Bật HTTPS và cấu hình cache behavior | 25/06/2026 | 25/06/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/> |
| 6   | - **Thực hành:** Thiết lập CloudWatch Dashboard <br>&emsp; + Tạo CloudWatch Dashboard cho giám sát SyncQuiz <br>&emsp; + Thêm widget: Lambda invocations và lỗi, API Gateway request count và latency, DynamoDB read/write capacity <br>&emsp; + Thêm CloudFront metrics: request count, error rate, cache hit ratio <br>&emsp; + Kiểm thử website đã deploy qua tên miền CloudFront <br>&emsp; + Xác minh SPA routing hoạt động đúng (không có lỗi 404 khi làm mới trang) | 26/06/2026 | 26/06/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |


### Kết quả đạt được tuần 10:

* Build và tối ưu React production bundle với code splitting và lazy loading được áp dụng.

* Deploy thành công frontend production lên Amazon S3.

* Cấu hình Amazon CloudFront Distribution với S3 origin và Origin Access Control để phân phối an toàn.

* Cập nhật S3 bucket policy để chặn truy cập công cộng trực tiếp, chỉ cho phép CloudFront phục vụ nội dung.

* Cấu hình custom error response hỗ trợ SPA routing — không có lỗi 404 khi làm mới trang.

* Tạo CloudWatch Dashboard với widget chính cho Lambda, API Gateway, DynamoDB và CloudFront metrics.

* Website đã deploy được kiểm thử qua CloudFront và xác nhận hoạt động đầy đủ.