---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---
### Week 5 Objectives:

* Deploy an Application Load Balancer to distribute traffic across multiple EC2 instances.
* Configure Auto Scaling Group with dynamic scaling policies for the application tier.
* Set up AWS Budgets and Cost Explorer to monitor and control cloud spending.
* Verify high availability by testing instance failure and automatic replacement.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Elastic Load Balancing: ALB vs NLB vs CLB <br> - Study ALB components: listeners, rules, target groups, health checks <br> - Study Auto Scaling Group: desired/min/max capacity, scaling policies (target tracking, step scaling, scheduled) | 05/18/2026 | 05/18/2026 | <https://docs.aws.amazon.com/elasticloadbalancing/> |
| 3   | - **Practice:** Create Application Load Balancer <br>&emsp; + Create Target Group (port 3000, HTTP health check on /health) <br>&emsp; + Create ALB in public subnets, configure listener on port 80 <br>&emsp; + Register EC2 instances to target group <br>&emsp; + Verify traffic is balanced across instances via ALB DNS name | 05/19/2026 | 05/19/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Create Auto Scaling Group <br>&emsp; + Create Launch Template with user data for app deployment <br>&emsp; + Configure ASG: min 2, desired 2, max 6 instances across 2 AZs <br>&emsp; + Attach ASG to ALB Target Group <br>&emsp; + Add Target Tracking Scaling policy (CPU utilization threshold: 60%) <br>&emsp; + Add Scale-In protection on new instances | 05/20/2026 | 05/20/2026 | <https://docs.aws.amazon.com/autoscaling/ec2/userguide/> |
| 5   | - **Practice:** AWS Budgets and Cost Management <br>&emsp; + Create monthly cost budget with email alert at 80% and 100% <br>&emsp; + Create usage budget for EC2 hours <br>&emsp; + Explore Cost Explorer: filter by service, tag, region <br>&emsp; + Enable Cost Allocation Tags for resource tracking | 05/21/2026 | 05/21/2026 | <https://docs.aws.amazon.com/cost-management/> |
| 6   | - **Load & Resilience Testing:** <br>&emsp; + Use Apache Bench (ab) to generate load and trigger scale-out <br>&emsp; + Observe ASG activity log: instances launching <br>&emsp; + Terminate an instance manually and verify ASG replaces it <br>&emsp; + Verify ALB health checks remove unhealthy instances <br> - Review scaling activity history and CloudWatch metrics | 05/22/2026 | 05/22/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 5 Achievements:

* Deployed an Application Load Balancer with a target group, health checks, and listener rules.

* Created an Auto Scaling Group with min/desired/max capacity spread across two Availability Zones.

* Configured Target Tracking scaling policy based on CPU utilization — scale-out triggered successfully under load.

* Verified high availability: terminated an instance and confirmed ASG automatically launched a replacement.

* Set up AWS Budgets with cost and usage alerts to proactively manage spending.

* Used Cost Explorer to analyze costs by service and applied cost allocation tags for granular tracking.