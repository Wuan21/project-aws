---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
### Week 9 Objectives:

* Containerize the Node.js application and deploy using Amazon ECS with AWS Fargate.
* Automate deployment pipeline with AWS CodePipeline and CodeDeploy blue/green strategy.
* Enable and configure AWS Security Hub to assess cloud security posture.
* Remediate critical security findings from CIS AWS Foundations Benchmark.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon ECS: clusters, task definitions, services, Fargate launch type <br> - Study Amazon ECR: repositories, image scanning, lifecycle policies <br> - **Practice:** Containerize Node.js app <br>&emsp; + Write Dockerfile (node:18-alpine base image) <br>&emsp; + Build image locally, test with docker run <br>&emsp; + Push image to Amazon ECR repository | 06/15/2026 | 06/15/2026 | <https://docs.aws.amazon.com/ecs/> |
| 3   | - **Practice:** Create ECS Cluster and Service on Fargate <br>&emsp; + Create ECS Cluster (Fargate + Fargate Spot capacity) <br>&emsp; + Create Task Definition: container image from ECR, 0.5 vCPU, 1 GB memory, env vars from Secrets Manager <br>&emsp; + Create ECS Service: desired count 2, rolling update deployment, attach to ALB target group <br>&emsp; + Verify containers healthy in ALB and ECS console | 06/16/2026 | 06/16/2026 | <https://docs.aws.amazon.com/ecs/latest/developerguide/> |
| 4   | - **Practice:** Build CI/CD pipeline with CodePipeline <br>&emsp; + Source: GitHub repository (CodeStar connection) <br>&emsp; + Build: CodeBuild project builds Docker image, pushes to ECR, generates imagedefinitions.json <br>&emsp; + Deploy: CodeDeploy blue/green deployment to ECS service <br>&emsp; + Test pipeline: push code commit → pipeline runs → new containers deployed automatically | 06/17/2026 | 06/17/2026 | <https://docs.aws.amazon.com/codepipeline/latest/userguide/> |
| 5   | - **Practice:** Enable AWS Security Hub <br>&emsp; + Enable Security Hub in the AWS account and region <br>&emsp; + Enable standards: AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark v1.4 <br>&emsp; + Review findings dashboard: Critical, High, Medium severity findings <br>&emsp; + Identify and prioritize top 5 critical findings | 06/18/2026 | 06/18/2026 | <https://docs.aws.amazon.com/securityhub/latest/userguide/> |
| 6   | - **Remediate Security Hub findings:** <br>&emsp; + Enable MFA on root account and all IAM users <br>&emsp; + Enable CloudTrail in all regions with S3 log validation <br>&emsp; + Remove overly permissive Security Group rules (0.0.0.0/0 on SSH) <br>&emsp; + Enable S3 bucket versioning and block public access <br> - Re-run Security Hub checks and document score improvement <br> - Review CodePipeline execution history | 06/19/2026 | 06/19/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 9 Achievements:

* Containerized the Node.js application using Docker and pushed the image to Amazon ECR with vulnerability scanning.

* Deployed ECS Service on Fargate with 2 running tasks, integrated with ALB for traffic distribution.

* Built and tested a full CI/CD pipeline: GitHub → CodeBuild → ECR → CodeDeploy blue/green to ECS.

* Enabled AWS Security Hub with CIS AWS Foundations and AWS Foundational Security Best Practices standards.

* Identified and remediated top critical findings: MFA enforcement, CloudTrail, overly permissive Security Groups.

* Security Hub compliance score improved after remediation of critical and high severity findings.