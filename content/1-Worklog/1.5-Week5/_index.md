---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---
### Week 5 Objectives:

* Practice combining the AWS services learned in previous weeks.
* Evaluate how AWS services can be integrated in the SyncQuiz architecture.
* Experiment with WebSocket API for real-time communication features.
* Prepare the initial architecture idea for the SyncQuiz real-time quiz system.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Review and consolidate knowledge of all AWS services studied in Weeks 1 to 4 <br> - Build a basic serverless backend flow using Lambda and API Gateway <br>&emsp; + Create multiple Lambda functions for different business operations <br>&emsp; + Create API Gateway routes and integrate each route with the appropriate Lambda function <br>&emsp; + Test end-to-end: send HTTP request → API Gateway → Lambda → return response | 05/18/2026 | 05/18/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Configure Cognito for user authentication management <br>&emsp; + Create a Cognito User Pool with email-based sign-in <br>&emsp; + Create an App Client and configure token settings <br>&emsp; + Test signup and login flow using the Cognito console <br>&emsp; + Test how frontend/backend services use Cognito tokens to call protected APIs | 05/19/2026 | 05/19/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Experiment with WebSocket API for real-time features <br>&emsp; + Create a WebSocket API in API Gateway with $connect, $disconnect, and $default routes <br>&emsp; + Create Lambda functions to handle each WebSocket route <br>&emsp; + Test WebSocket connection using a WebSocket client tool <br>&emsp; + Send messages and verify Lambda receives and responds to WebSocket events | 05/20/2026 | 05/20/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 5   | - Monitor logs and errors using CloudWatch <br>&emsp; + Review CloudWatch Logs for Lambda functions invoked in the integration test <br>&emsp; + Identify and resolve errors discovered during testing <br>&emsp; + Review CloudWatch Metrics for API Gateway request counts and Lambda error rates <br>&emsp; + Add additional log statements to Lambda functions for better observability | 05/21/2026 | 05/21/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Evaluate how AWS services can be combined in the SyncQuiz architecture <br>&emsp; + Map each SyncQuiz feature to the appropriate AWS service <br>&emsp; + Draft the initial high-level architecture diagram for SyncQuiz <br>&emsp; + Identify open technical questions and challenges to resolve in the project phase <br>&emsp; + Prepare the initial architecture idea and present it as the SyncQuiz Project Proposal | 05/22/2026 | 05/22/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 5 Achievements:

* Practiced integrating the AWS services studied in previous weeks to better understand how they work in a real-world system.

* Built a basic serverless backend flow using Lambda and API Gateway, successfully testing HTTP request routing to Lambda functions.

* Configured a Cognito User Pool and App Client, tested the signup and login flow, and verified how Cognito tokens protect API routes.

* Experimented with API Gateway WebSocket API, created a working WebSocket connection, and verified that Lambda correctly handles WebSocket messages.

* Monitored Lambda and API Gateway behavior using CloudWatch Logs and CloudWatch Metrics, identifying and resolving errors during integration testing.

* Evaluated how Cognito, API Gateway, Lambda, WebSocket API, and CloudWatch can be applied to the SyncQuiz project, and prepared the initial architecture idea for the real-time quiz system.