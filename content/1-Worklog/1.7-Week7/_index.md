---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
### Week 7 Objectives:

* Understand Amazon SNS and SQS messaging and notification services.
* Integrate SNS to send real-time notifications on application events.
* Build a reliable fanout notification pattern using SNS and SQS.
* Test notification delivery across multiple subscription types.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon SNS: topics, subscriptions (email, SMS, HTTP/S, Lambda, SQS), message filtering <br> - Study Amazon SQS: standard queues vs FIFO queues, visibility timeout, dead-letter queues <br> - Study SNS + SQS fanout pattern for decoupled message delivery | 06/01/2026 | 06/01/2026 | <https://docs.aws.amazon.com/sns/latest/dg/> |
| 3   | - **Practice:** Create SNS topic and subscriptions <br>&emsp; + Create SNS Standard topic `AppNotifications` <br>&emsp; + Add email subscription and confirm via inbox <br>&emsp; + Add SMS subscription (E.164 phone number) <br>&emsp; + Publish test message and verify delivery to all subscribers <br>&emsp; + Configure message filter policies per subscription | 06/02/2026 | 06/02/2026 | <https://docs.aws.amazon.com/sns/latest/dg/sns-getting-started.html> |
| 4   | - **Practice:** Integrate SNS into application <br>&emsp; + Add AWS SDK v3 SNS client to Node.js app <br>&emsp; + Publish SNS message on events: new high score, user achievement unlocked <br>&emsp; + Include structured message attributes (userId, eventType, score) <br>&emsp; + Write Lambda subscriber that processes SNS events and logs to CloudWatch | 06/03/2026 | 06/03/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Practice:** Build SQS buffer for async processing <br>&emsp; + Create SQS Standard queue `ScoreQueue` and subscribe to SNS topic <br>&emsp; + Create SQS Dead Letter Queue for failed messages (maxReceiveCount: 3) <br>&emsp; + Configure Lambda to poll SQS queue (event source mapping) <br>&emsp; + Test: publish SNS → SQS delivers to Lambda → Lambda processes and logs | 06/04/2026 | 06/04/2026 | <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/> |
| 6   | - Test failure scenarios: <br>&emsp; + Simulate Lambda processing failure → message moves to DLQ after 3 retries <br>&emsp; + Test SQS visibility timeout with slow consumer <br>&emsp; + Verify DLQ message inspection and re-drive policy <br> - Benchmark SNS delivery latency (email, SMS, Lambda) <br> - Document notification architecture | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 7 Achievements:

* Created and configured SNS topic with email, SMS, and SQS subscription types.

* Successfully delivered notifications via SNS on application events (new high score, achievement unlocked).

* Implemented message filter policies to route specific event types to targeted subscribers.

* Built an SQS Standard queue as SNS fanout buffer, with Dead Letter Queue for error handling.

* Configured Lambda event source mapping to process SQS messages asynchronously.

* Tested DLQ behavior: messages correctly moved after 3 failed processing attempts.