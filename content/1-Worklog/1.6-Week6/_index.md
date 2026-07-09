---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
### Week 6 Objectives:

* Design a gamification system for user engagement using AWS serverless services.
* Implement scoring logic with AWS Lambda and store leaderboard data in DynamoDB.
* Expose leaderboard functionality via Amazon API Gateway.
* Test end-to-end scoring and ranking flow.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon DynamoDB: tables, partition keys, sort keys, GSI, LSI <br> - Study AWS Lambda: execution model, triggers, environment variables, layers <br> - Design gamification data model: user scores, achievements, leaderboard ranking | 05/25/2026 | 05/25/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 3   | - **Practice:** Set up DynamoDB leaderboard <br>&emsp; + Create DynamoDB table `leaderboard` (partition key: userId, sort key: timestamp) <br>&emsp; + Create GSI on `score` attribute for ranked queries <br>&emsp; + Write Lambda function `submitScore`: validates input, writes item to DynamoDB <br>&emsp; + Test Lambda locally using SAM CLI | 05/26/2026 | 05/26/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/> |
| 4   | - **Practice:** Build leaderboard query Lambda <br>&emsp; + Write Lambda function `getLeaderboard`: queries DynamoDB GSI ordered by score desc <br>&emsp; + Add pagination support (Limit + ExclusiveStartKey) <br>&emsp; + Create API Gateway REST API with resources `/score` (POST) and `/leaderboard` (GET) <br>&emsp; + Configure Lambda proxy integration for each route | 05/27/2026 | 05/27/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |
| 5   | - Integrate API Gateway with Node.js frontend <br>&emsp; + Add API key authentication to API Gateway <br>&emsp; + Update CORS settings to allow frontend origin <br>&emsp; + Deploy API to `prod` stage <br> - Test full flow: submit score → DynamoDB → query leaderboard API | 05/28/2026 | 05/28/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Add achievement system: Lambda checks milestones (e.g., top 10) and writes to `achievements` table <br> - Configure DynamoDB Streams to trigger achievement Lambda on new score entry <br> - Load test: submit 100 concurrent scores, verify DynamoDB and API consistency <br> - Review Lambda cold start times and optimize with Provisioned Concurrency | 05/29/2026 | 05/29/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html> |


### Week 6 Achievements:

* Designed and implemented a serverless gamification system using Lambda, DynamoDB, and API Gateway.

* Created DynamoDB table with Global Secondary Index for efficient leaderboard queries by score.

* Developed and deployed Lambda functions for score submission and leaderboard retrieval.

* Exposed leaderboard APIs via API Gateway with API key authentication and CORS configuration.

* Implemented DynamoDB Streams to trigger achievement checks on new score entries.

* Load tested the system with 100 concurrent score submissions — all records consistent.