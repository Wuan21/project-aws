---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Deploy the Next.js frontend (host and player interfaces) on AWS Amplify and set up Git-based automated CI/CD.
* Integrate Amazon Cognito User Pool for secure host authentication (teachers/quiz creators) and player session tracking.
* Deploy and automate the CI/CD pipeline for the backend WebSocket API (API Gateway WebSocket) and Lambda handlers processing real-time events (Join Room, Submit Answer, Get Leaderboard) using GitHub Actions.
* Set up a real-time monitoring system using CloudWatch Dashboards to track concurrent WebSocket connections, message traffic, and Lambda execution metrics.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn and configure AWS Amplify Hosting for the Next.js frontend of SyncQuizz <br> - Integrate with GitHub repository to enable automatic build-on-commit to the `main` branch <br> - Customize the `amplify.yml` build configuration to optimize dependencies installation, application building, and cache parameters | 06/29/2026 | 06/29/2026 | <https://docs.aws.amazon.com/amplify/> |
| 3 | - Configure Amazon Cognito User Pool and Client to integrate login/register authentication for Host accounts <br> - Design CI/CD workflow using GitHub Actions (integrating SAM or Serverless Framework) to package and deploy serverless backend resources <br> - Configure secure AWS credentials in GitHub Secrets | 06/30/2026 | 06/30/2026 | <https://docs.aws.amazon.com/cognito/> |
| 4 | - Execute the full deployment pipeline for SyncQuizz: Next.js frontend on Amplify and API Gateway WebSocket/REST API backend resources <br> - Map environment variables (WebSocket URL, Cognito Client ID) to the frontend application <br> - Configure CORS rules on API Gateway to accept frontend origins | 07/01/2026 | 07/01/2026 | <https://docs.github.com/en/actions/> |
| 5 | - Build a unified CloudWatch Dashboard to monitor SyncQuizz operations: track concurrent WebSocket connections (`ConnectCount`), message throughput, and resource usage <br> - Measure Lambda execution metrics (invocations, errors, and duration) for connection handlers <br> - Configure CloudWatch Metrics for DynamoDB tables to track capacity performance during concurrent user submissions | 07/02/2026 | 07/02/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |
| 6 | - Conduct end-to-end integration tests: simulate host creating a lobby, players joining via WebSockets, answering questions, and updating leaderboard rankings in real-time <br> - Perform light load testing (simulating 50-100 concurrent clients) and observe system metrics on the dashboard <br> - Finalize architecture diagrams, WebSocket data flow schemes, and operational runbooks | 07/03/2026 | 07/03/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 11 Achievements:

* Successfully deployed the Next.js frontend on AWS Amplify with a Git-triggered automated CI/CD pipeline from GitHub.

* Integrated Amazon Cognito User Pool for secure host authentication and reliable session identification of participants.

* Configured a GitHub Actions workflow to automate the deployment of backend WebSocket APIs, Lambda functions, and DynamoDB tables.

* Designed a comprehensive CloudWatch Dashboard monitoring concurrent WebSockets connections, Lambda performance, and database write capacity in real-time.

* Validated real-time quiz synchronization between the Host dashboard and player devices with minimal latency under simulated load.

