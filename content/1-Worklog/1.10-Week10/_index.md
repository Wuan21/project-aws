---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Connect multiple VPCs using VPC Peering and AWS Transit Gateway.
* Understand routing and security implications for multi-VPC architectures.
* Automate operational tasks using AWS Lambda and Amazon EventBridge.
* Build event-driven workflows for scheduled and reactive automation.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study VPC Peering: how it works, routing requirements, limitations (no transitive routing) <br> - Study AWS Transit Gateway: attachments, route tables, centralized routing hub <br> - Compare VPC Peering vs Transit Gateway: scale, cost, use cases | 06/22/2026 | 06/22/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/> |
| 3   | - **Practice:** VPC Peering <br>&emsp; + Create a second VPC (10.1.0.0/16) with private subnets <br>&emsp; + Create VPC Peering connection between VPC-A and VPC-B <br>&emsp; + Accept peering request and update route tables in both VPCs <br>&emsp; + Launch EC2 instances in each VPC and test ping/SSH across peering <br>&emsp; + Verify security group allows traffic from the peered VPC CIDR | 06/23/2026 | 06/23/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/create-vpc-peering-connection.html> |
| 4   | - **Practice:** AWS Transit Gateway <br>&emsp; + Create Transit Gateway with ECMP and DNS support enabled <br>&emsp; + Attach VPC-A and VPC-B to Transit Gateway <br>&emsp; + Create a third VPC (10.2.0.0/16) and attach to TGW <br>&emsp; + Configure TGW route table to route traffic between all 3 VPCs <br>&emsp; + Test full mesh connectivity: VPC-A ↔ VPC-B ↔ VPC-C via TGW | 06/24/2026 | 06/24/2026 | <https://docs.aws.amazon.com/vpc/latest/tgw/> |
| 5   | - **Practice:** Lambda automation with EventBridge <br>&emsp; + Write Lambda `StopDevInstances`: queries EC2 by tag (Env=dev), stops all instances <br>&emsp; + Write Lambda `StartDevInstances`: starts tagged dev instances <br>&emsp; + Create EventBridge Scheduled Rules: Stop at 20:00, Start at 08:00 weekdays <br>&emsp; + Grant Lambda role: ec2:StopInstances, ec2:StartInstances, ec2:DescribeInstances (scoped by tag) | 06/25/2026 | 06/25/2026 | <https://docs.aws.amazon.com/eventbridge/latest/userguide/> |
| 6   | - **Practice:** Reactive Lambda automation <br>&emsp; + Write Lambda `CleanOldSnapshots`: deletes EBS snapshots older than 30 days <br>&emsp; + Trigger via EventBridge scheduled rule (weekly) <br>&emsp; + Write Lambda `NotifyOnBudgetAlert`: triggered by SNS from AWS Budgets alarm, sends formatted Slack webhook <br> - Review IAM least-privilege policies for all Lambda roles <br> - Document the full automation architecture | 06/26/2026 | 06/26/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 10 Achievements:

* Understood what AWS is and mastered the basic service groups: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

### Week 10 Achievements:

* Established VPC Peering between two VPCs with proper route table updates and security group rules.

* Configured Transit Gateway and connected three VPCs, enabling full mesh connectivity.

* Automated EC2 start/stop scheduling for dev instances using Lambda and EventBridge — estimated cost saving from reduced idle hours.

* Automated EBS snapshot cleanup: Lambda deletes snapshots older than 30 days on a weekly schedule.

* Implemented budget alert Lambda that sends formatted Slack webhook notifications when cost thresholds are breached.

* Applied least-privilege IAM policies to all Lambda execution roles, scoped by resource tags.

