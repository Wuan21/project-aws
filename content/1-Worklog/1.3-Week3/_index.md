---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
### Week 3 Objectives:

* Manage EC2 Linux and Windows instances effectively in the VPC.
* Deploy a Node.js web application on an EC2 instance.
* Understand AMI creation, Launch Templates, and Elastic IP management.
* Configure Security Groups and access controls for web applications.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study EC2 advanced features: AMI lifecycle, Launch Templates, Instance Metadata Service <br> - Review Windows EC2: RDP connection, key-pair password decryption <br> - Study Placement Groups (cluster, spread, partition) | 05/04/2026 | 05/04/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/> |
| 3   | - **Practice:** Launch and manage EC2 instances <br>&emsp; + Launch Amazon Linux 2 instance in public subnet <br>&emsp; + Launch Windows Server 2022 instance, retrieve password, connect via RDP <br>&emsp; + Compare instance management between Linux and Windows <br>&emsp; + Create custom AMI from configured Linux instance | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Deploy Node.js application on Linux EC2 <br>&emsp; + Install Node.js (v18 LTS) via nvm <br>&emsp; + Clone sample Express.js application <br>&emsp; + Configure environment variables (DB host, port, secrets) <br>&emsp; + Install PM2 process manager and start app <br>&emsp; + Configure Security Group to allow HTTP port 3000 | 05/06/2026 | 05/06/2026 | <https://nodejs.org/en/docs> |
| 5   | - Configure Nginx as a reverse proxy for Node.js app <br>&emsp; + Install and configure Nginx <br>&emsp; + Proxy HTTP port 80 to Node.js port 3000 <br>&emsp; + Configure Security Group: allow HTTP (80) and HTTPS (443) <br> - Set up PM2 to restart app on reboot <br> - Allocate Elastic IP and associate with instance | 05/07/2026 | 05/07/2026 | <https://www.nginx.com/resources/wiki/> |
| 6   | - **Practice:** Create Launch Template for repeatable EC2 deployments <br>&emsp; + Configure instance type, AMI, subnet, Security Group, user data script <br>&emsp; + User data: auto-install Node.js and start app on boot <br> - Test application end-to-end via Elastic IP and Nginx <br> - Document deployment steps | 05/08/2026 | 05/08/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 3 Achievements:

* Successfully launched and managed both Linux (Amazon Linux 2) and Windows Server (2022) EC2 instances.

* Connected to Linux via SSH and Windows via RDP after decrypting the administrator password.

* Deployed a Node.js (Express.js) application on EC2 with PM2 as the process manager.

* Configured Nginx as a reverse proxy to expose the application on port 80.

* Created a custom AMI and a Launch Template with user data for automated deployments.

* Associated an Elastic IP to provide a stable endpoint for the web application.