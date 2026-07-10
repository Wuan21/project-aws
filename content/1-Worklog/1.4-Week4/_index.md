---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---
### Week 4 Objectives:

* Learn about Amazon CloudWatch for monitoring logs, metrics, and system status.
* Learn about Amazon SQS and the message queue mechanism.
* Learn about Amazon SNS and the publish/subscribe notification model.
* Compare the roles of SQS and SNS in distributed system architecture.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon CloudWatch: overview and core features <br>&emsp; + CloudWatch Logs: viewing and filtering log streams from Lambda and other services <br>&emsp; + CloudWatch Metrics: monitoring service metrics such as Lambda invocations, errors, and duration <br>&emsp; + CloudWatch Alarms: setting threshold-based alerts for automated notifications | 05/11/2026 | 05/11/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/> |
| 3   | - **Practice:** View Lambda logs and create a CloudWatch Dashboard <br>&emsp; + Trigger a Lambda function and view its execution logs in CloudWatch Logs <br>&emsp; + Explore Log Groups and Log Streams for a Lambda function <br>&emsp; + Create a basic CloudWatch Dashboard with widgets for Lambda metrics <br>&emsp; + Add an alarm for Lambda error count | 05/12/2026 | 05/12/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Study Amazon SQS and the message queue mechanism <br>&emsp; + SQS Standard Queue vs FIFO Queue: differences in ordering and delivery guarantees <br>&emsp; + Visibility timeout: preventing duplicate processing of in-flight messages <br>&emsp; + Dead Letter Queue (DLQ): handling failed messages after maximum retries <br>&emsp; + Long polling: reducing empty API calls when the queue is idle | 05/13/2026 | 05/13/2026 | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| 5   | - **Practice:** Create an SQS queue and test message sending/receiving <br>&emsp; + Create an SQS Standard Queue <br>&emsp; + Send messages using the AWS Console and AWS CLI <br>&emsp; + Receive and delete messages manually <br>&emsp; + Create a Dead Letter Queue and configure redrive policy (maxReceiveCount: 3) | 05/14/2026 | 05/14/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Study Amazon SNS and the publish/subscribe model <br>&emsp; + Topics and subscriptions: email, SMS, HTTP/S, Lambda, and SQS <br>&emsp; + Message filtering policies: routing messages to specific subscribers <br> - **Practice:** Create a topic and send notifications through SNS <br>&emsp; + Create an SNS Standard Topic <br>&emsp; + Add an email subscription and confirm <br>&emsp; + Publish a test message and verify delivery <br> - Compare SQS and SNS: purpose, delivery model, and use in distributed systems | 05/15/2026 | 05/15/2026 | <https://docs.aws.amazon.com/sns/latest/dg/> |


### Week 4 Achievements:

* Learned Amazon CloudWatch and understood how to monitor logs and metrics for AWS services such as Lambda through CloudWatch Logs and CloudWatch Metrics.

* Successfully practiced viewing Lambda execution logs in CloudWatch and created a basic CloudWatch Dashboard with alarms for Lambda error monitoring.

* Studied Amazon SQS and understood Standard Queue vs FIFO Queue, visibility timeout, Dead Letter Queue, and long polling.

* Practiced creating an SQS queue, sending and receiving messages using both the AWS Console and CLI, and configuring a Dead Letter Queue with a redrive policy.

* Learned Amazon SNS and the publish/subscribe model, practiced creating an SNS topic with email subscription, and verified notification delivery.

* Compared SQS and SNS, understanding the appropriate role of each service in asynchronous message processing and notification delivery in distributed system architecture.