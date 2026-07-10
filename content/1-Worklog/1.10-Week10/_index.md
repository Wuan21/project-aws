---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Build and optimize the production frontend bundle.
* Deploy the frontend to Amazon S3 with CloudFront distribution.
* Configure Origin Access Control and bucket policy for secure delivery.
* Set up a CloudWatch Dashboard for system monitoring.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Review production build requirements for the React frontend <br> - Study Amazon S3 static website hosting configuration <br> - Study Amazon CloudFront: distributions, origins, behaviors, caching, HTTPS, and error pages | 06/22/2026 | 06/22/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| 3   | - **Practice:** Build and optimize the production bundle <br>&emsp; + Run production build (npm run build / vite build) <br>&emsp; + Analyze bundle size and identify large dependencies <br>&emsp; + Apply code splitting and lazy loading for route-based chunks <br>&emsp; + Minify JavaScript and CSS, enable gzip/brotli compression settings <br>&emsp; + Verify build output: index.html, assets/, correct file structure | 06/23/2026 | 06/23/2026 | <https://vitejs.dev/guide/build.html> |
| 4   | - **Practice:** Deploy frontend to Amazon S3 <br>&emsp; + Create S3 bucket with the project naming convention <br>&emsp; + Disable public access block (to allow CloudFront access via OAC) <br>&emsp; + Upload production build files to S3 bucket <br>&emsp; + Verify files are correctly uploaded and accessible internally | 06/24/2026 | 06/24/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| 5   | - **Practice:** Configure CloudFront Distribution <br>&emsp; + Create CloudFront distribution with S3 origin <br>&emsp; + Configure Origin Access Control (OAC) and update S3 bucket policy <br>&emsp; + Set default root object to index.html <br>&emsp; + Configure custom error response: 403/404 → /index.html (for SPA routing) <br>&emsp; + Enable HTTPS and configure cache behaviors | 06/25/2026 | 06/25/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/> |
| 6   | - **Practice:** Set up CloudWatch Dashboard <br>&emsp; + Create CloudWatch Dashboard for SyncQuiz monitoring <br>&emsp; + Add widgets: Lambda invocations and errors, API Gateway request count and latency, DynamoDB read/write capacity <br>&emsp; + Add CloudFront metrics: request count, error rate, cache hit ratio <br>&emsp; + Test the deployed website through CloudFront domain name <br>&emsp; + Verify SPA routing works correctly (no 404 on page refresh) | 06/26/2026 | 06/26/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |


### Week 10 Achievements:

* Built and optimized the React production bundle with code splitting and lazy loading applied.

* Successfully deployed the production frontend to Amazon S3.

* Configured Amazon CloudFront Distribution with the S3 origin and Origin Access Control for secure delivery.

* Updated the S3 bucket policy to restrict direct public access, allowing only CloudFront to serve content.

* Configured custom error responses for SPA routing support — no 404 errors on page refresh.

* Created a CloudWatch Dashboard with key widgets for Lambda, API Gateway, DynamoDB, and CloudFront metrics.

* The deployed website was tested through CloudFront and confirmed to be fully functional.
