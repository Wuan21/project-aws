---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
### Week 2 Objectives:

* Understand VPC architecture concepts: CIDR, subnets, routing, and gateways.
* Design and deploy a complete VPC with public and private subnets across multiple AZs.
* Configure Security Groups, NACLs, Internet Gateway, and NAT Gateway.
* Verify inter-subnet connectivity and internet access from instances.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study VPC fundamentals: CIDR blocks, IPv4/IPv6 addressing <br> - Understand subnet types (public vs private), route tables, and availability zones <br> - Review VPC default vs custom VPC differences | 04/27/2026 | 04/27/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/> |
| 3   | - **Practice:** Create a custom VPC (10.0.0.0/16) <br>&emsp; + Create 2 public subnets in different AZs (10.0.1.0/24, 10.0.2.0/24) <br>&emsp; + Create 2 private subnets in different AZs (10.0.3.0/24, 10.0.4.0/24) <br>&emsp; + Attach an Internet Gateway to the VPC <br>&emsp; + Configure public route tables to route 0.0.0.0/0 to IGW | 04/28/2026 | 04/28/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Configure outbound internet for private subnets <br>&emsp; + Create a NAT Gateway in a public subnet with an Elastic IP <br>&emsp; + Update private route table to route 0.0.0.0/0 to NAT Gateway <br>&emsp; + Configure Security Groups: allow HTTP/HTTPS from ALB, SSH from bastion host <br>&emsp; + Configure Network ACLs for subnet-level protection | 04/29/2026 | 04/29/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html> |
| 5   | - Deploy a bastion host (EC2) in the public subnet <br> - Launch an EC2 instance in the private subnet <br> - Verify SSH connectivity: local → bastion → private instance <br> - Test outbound internet access from private instance through NAT Gateway | 04/30/2026 | 04/30/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Review and finalize VPC architecture diagram <br> - **Practice:** Enable VPC Flow Logs to CloudWatch Logs <br>&emsp; + Create Flow Log for the VPC <br>&emsp; + Query flow logs to analyze traffic patterns <br> - Document the full VPC design | 05/01/2026 | 05/01/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html> |


### Week 2 Achievements:

* Designed and deployed a production-style VPC with public and private subnets across two Availability Zones.

* Configured Internet Gateway and NAT Gateway for appropriate inbound and outbound internet access.

* Secured resources using Security Groups (instance-level) and Network ACLs (subnet-level).

* Deployed a bastion host and successfully accessed a private EC2 instance via SSH jump.

* Enabled and queried VPC Flow Logs in CloudWatch to analyze network traffic.

* Verified complete connectivity: public subnet to internet, private subnet via NAT, and internal subnets.