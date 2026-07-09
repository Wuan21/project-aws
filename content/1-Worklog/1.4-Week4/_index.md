---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---
### Week 4 Objectives:

* Understand Amazon RDS managed database service and its key features.
* Deploy an Amazon RDS MySQL instance in a private subnet.
* Connect the Node.js application to RDS and verify database operations.
* Practice automated backup, manual snapshots, and point-in-time restore.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon RDS: supported engines (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora) <br> - Study RDS deployment options: Single-AZ, Multi-AZ, Read Replicas <br> - Study RDS pricing: instance types, storage (gp3, io1), data transfer <br> - Study RDS Parameter Groups and Option Groups | 05/11/2026 | 05/11/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/> |
| 3   | - **Practice:** Create RDS MySQL 8.0 instance <br>&emsp; + Create DB Subnet Group (private subnets across 2 AZs) <br>&emsp; + Launch RDS with Multi-AZ enabled, gp3 storage <br>&emsp; + Configure Security Group: allow MySQL port 3306 from EC2 Security Group only <br>&emsp; + Enable automated backups (retention: 7 days) and maintenance window | 05/12/2026 | 05/12/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/USER_CreateDBInstance.html> |
| 4   | - **Practice:** Connect application to RDS <br>&emsp; + SSH to EC2 instance, install MySQL client <br>&emsp; + Connect to RDS endpoint, create database and tables <br>&emsp; + Update Node.js app environment variables (DB_HOST, DB_NAME, DB_USER, DB_PASS) <br>&emsp; + Test CRUD operations from the app to RDS <br> - Enable RDS Enhanced Monitoring and Performance Insights | 05/13/2026 | 05/13/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Study RDS backup and recovery strategies <br> - **Practice:** Backup and Restore <br>&emsp; + Create a manual DB snapshot <br>&emsp; + Modify database records to simulate data change <br>&emsp; + Restore RDS from snapshot to a new instance <br>&emsp; + Verify data consistency after restore | 05/14/2026 | 05/14/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/USER_RestoreFromSnapshot.html> |
| 6   | - **Practice:** Test RDS Multi-AZ failover <br>&emsp; + Trigger a manual failover via console <br>&emsp; + Measure failover time (DNS propagation) <br>&emsp; + Verify application reconnects automatically <br> - Create Read Replica in a different AZ <br> - Review costs and optimize storage autoscaling settings | 05/15/2026 | 05/15/2026 | <https://docs.aws.amazon.com/rds/latest/userguide/Concepts.MultiAZ.html> |


### Week 4 Achievements:

* Understood Amazon RDS features: supported engines, Multi-AZ, Read Replicas, and automated backups.

* Deployed RDS MySQL 8.0 in a private subnet group with Multi-AZ enabled for high availability.

* Secured database access using Security Group rules scoped to the EC2 application tier only.

* Connected the Node.js application to RDS and verified full CRUD operation functionality.

* Created manual snapshots, restored a database from a snapshot, and verified data integrity.

* Triggered and measured Multi-AZ failover and confirmed application auto-reconnect behavior.