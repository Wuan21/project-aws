---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Objectives:

* Monitor application and infrastructure health using Amazon CloudWatch.
* Create CloudWatch Alarms for API error rate and SQS queue depth thresholds.
* Deliver operational alerts to administrators through SNS notifications.
* Use CloudWatch Dashboards and Log Insights for observability.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study CloudWatch fundamentals: Metrics, Namespaces, Dimensions, Statistics <br> - Study CloudWatch Alarms: threshold types (static, anomaly detection), evaluation periods <br> - Study CloudWatch Logs: log groups, log streams, metric filters, retention policies <br> - Review key metrics: ALB 5XXCount, SQS ApproximateNumberOfMessagesNotVisible, Lambda Errors | 06/08/2026 | 06/08/2026 | <https://docs.aws.amazon.com/cloudwatch/> |
| 3   | - **Practice:** Create CloudWatch Alarms <br>&emsp; + Alarm 1: ALB `HTTPCode_ELB_5XX_Count` > 10 in 5 minutes → ALARM state <br>&emsp; + Alarm 2: SQS `ApproximateNumberOfMessagesNotVisible` > 100 → ALARM state <br>&emsp; + Alarm 3: Lambda `Errors` > 5 in 1 minute → ALARM state <br>&emsp; + Configure SNS topic as alarm action for email alerts to admin | 06/09/2026 | 06/09/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html> |
| 4   | - **Practice:** Build CloudWatch Dashboard <br>&emsp; + Add widgets: ALB Request Count, 5XX errors, Target Response Time <br>&emsp; + Add SQS queue depth and Lambda invocation/error rate <br>&emsp; + Add RDS CPU utilization and DB connections <br>&emsp; + Configure auto-refresh interval (1 minute) <br> - Create CloudWatch Log Group metric filter for application error keywords | 06/10/2026 | 06/10/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html> |
| 5   | - **Practice:** Simulate alarm conditions <br>&emsp; + Inject HTTP 500 errors via API to trigger ALB 5XX alarm <br>&emsp; + Pause SQS consumer Lambda to let messages accumulate <br>&emsp; + Verify SNS email alerts received within alarm evaluation period <br> - Use CloudWatch Log Insights to query: `stats count(*) by errorType | sort count desc` | 06/11/2026 | 06/11/2026 | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html> |
| 6   | - Configure Composite Alarm combining API error + SQS depth conditions <br> - Set up CloudWatch Contributor Insights on ALB access logs <br> - Enable Container Insights for ECS (preparation for Week 9) <br> - Review and tune alarm thresholds based on baseline metrics <br> - Document monitoring and alerting runbook | 06/12/2026 | 06/12/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 8 Achievements:

* Configured CloudWatch Alarms for ALB 5XX error rate, SQS queue backlog, and Lambda error rate.

* Successfully received SNS email alerts when alarm thresholds were breached during simulation tests.

* Built a multi-service CloudWatch Dashboard for real-time visibility of application health.

* Used CloudWatch Log Insights to query application logs and identify top error patterns.

* Created a Composite Alarm combining multiple conditions to reduce alert noise.

* Documented an operational runbook for alarm response procedures.