---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:

* Container hóa ứng dụng Node.js và triển khai trên Amazon ECS với AWS Fargate.
* Tự động hóa pipeline triển khai bằng CodePipeline và chiến lược blue/green của CodeDeploy.
* Bật và cấu hình AWS Security Hub để đánh giá trạng thái bảo mật cloud.
* Khắc phục các phát hiện bảo mật nghiêm trọng từ CIS AWS Foundations Benchmark.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Amazon ECS: cluster, task definition, service, Fargate launch type <br> - Tìm hiểu Amazon ECR: repository, image scanning, lifecycle policy <br> - **Thực hành:** Container hóa ứng dụng Node.js <br>&emsp; + Viết Dockerfile (base image node:18-alpine) <br>&emsp; + Build image cục bộ, test với docker run <br>&emsp; + Push image lên Amazon ECR repository | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/ecs/> |
| 3   | - **Thực hành:** Tạo ECS Cluster và Service trên Fargate <br>&emsp; + Tạo ECS Cluster (Fargate + Fargate Spot capacity) <br>&emsp; + Tạo Task Definition: container image từ ECR, 0.5 vCPU, 1 GB memory, env vars từ Secrets Manager <br>&emsp; + Tạo ECS Service: desired count 2, rolling update, gắn với ALB target group <br>&emsp; + Xác minh container healthy trong ALB và ECS console | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/ecs/latest/developerguide/> |
| 4   | - **Thực hành:** Xây dựng CI/CD pipeline với CodePipeline <br>&emsp; + Source: GitHub repository (kết nối CodeStar) <br>&emsp; + Build: CodeBuild project build Docker image, push lên ECR, tạo imagedefinitions.json <br>&emsp; + Deploy: CodeDeploy blue/green deployment đến ECS service <br>&emsp; + Test pipeline: push code commit → pipeline chạy → container mới tự động deploy | 17/06/2026 | 17/06/2026 | <https://docs.aws.amazon.com/codepipeline/latest/userguide/> |
| 5   | - **Thực hành:** Bật AWS Security Hub <br>&emsp; + Bật Security Hub trong account và region <br>&emsp; + Bật các chuẩn: AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark v1.4 <br>&emsp; + Xem dashboard phát hiện: Critical, High, Medium severity <br>&emsp; + Xác định và ưu tiên 5 phát hiện critical hàng đầu | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/securityhub/latest/userguide/> |
| 6   | - **Khắc phục phát hiện Security Hub:** <br>&emsp; + Bật MFA cho root account và tất cả IAM user <br>&emsp; + Bật CloudTrail toàn region với S3 log validation <br>&emsp; + Xóa rule Security Group quá rộng (0.0.0.0/0 trên SSH) <br>&emsp; + Bật S3 bucket versioning và block public access <br> - Chạy lại kiểm tra Security Hub và ghi lại điểm cải thiện <br> - Xem lại lịch sử thực thi CodePipeline | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

* Container hóa ứng dụng Node.js bằng Docker và push image lên ECR với quét lỗ hổng tự động.

* Triển khai ECS Service trên Fargate với 2 task đang chạy, tích hợp ALB phân phối traffic.

* Xây dựng và test CI/CD pipeline đầy đủ: GitHub → CodeBuild → ECR → CodeDeploy blue/green.

* Bật AWS Security Hub với chuẩn CIS AWS Foundations và AWS Foundational Security Best Practices.

* Xác định và khắc phục phát hiện critical: bật MFA, CloudTrail, loại bỏ Security Group quá rộng.

* Điểm tuân thủ Security Hub cải thiện sau khi khắc phục phát hiện critical và high severity.