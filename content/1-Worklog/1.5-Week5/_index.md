---
title: "Week 5: AWS Databases (RDS, Aurora, DynamoDB & ElastiCache)"
date: 2026-10-12
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Understand AWS Purpose-Built Databases and when to apply relational vs. NoSQL engines.
* Practice deploying Amazon RDS and explore Amazon Aurora (Multi-AZ, Read Replicas, automated backups).
* Master Amazon DynamoDB (Partition Keys, Sort Keys, GSIs, Read/Write Capacity Modes, Console & Boto3 CRUD) alongside Amazon ElastiCache.
* Integrate a sample web application with S3 & DynamoDB, publish Blogs 1 and 3, and clean up test resources.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Study AWS Purpose-Built Databases: Relational, Key-Value, Document, Graph, and In-Memory. <br> - Compare operational overhead of self-managed EC2 databases vs. AWS Managed Databases. <br> - Explore serverless query engines such as Amazon Athena. | 12/10/2026 | 12/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Tue | - Learn Amazon RDS and Amazon Aurora architectures (storage auto-scaling, Aurora Serverless). <br> - Launch an RDS DB Instance inside a Private Subnet, configure Security Groups, and test connectivity. <br> - Review Multi-AZ Failover, Read Replicas, and Automated Backups / Snapshots. | 13/10/2026 | 13/10/2026 | <https://000005.awsfcaj.com/> <br> <https://docs.aws.amazon.com/rds/> |
| Wed | - Study Partition Keys, Sort Keys, Global Secondary Indexes (GSIs), Read Consistency, and Capacity Modes in DynamoDB. <br> - Create a DynamoDB table and practice inserting, reading, and updating items via the AWS Console. <br> - Use AWS CloudShell and Python SDK (Boto3) for CRUD, Query, Scan, GSI creation, and resource cleanup. | 14/10/2026 | 14/10/2026 | <https://000060.awsfcaj.com/> <br> <https://000039.awsfcaj.com/> |
| Thu | - Study Amazon ElastiCache for Redis: create Subnet Groups, launch a Redis Cluster, and test Set/Get, Hash, and Pub/Sub operations. <br> - Connect a sample web app to Amazon S3 and DynamoDB using IAM Roles without static keys. <br> - Finalize **Blog 3** (*Amazon Linux AMI vs. Windows AMI*). | 15/10/2026 | 15/10/2026 | <https://000061.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Fri | - Evaluate database selection matrices across application patterns and pass Module 3 quiz on Coursera. <br> - Finalize **Blog 1** (*Centralized Management of AWS Accounts with Organizations & SCPs*). <br> - Clean up temporary RDS instances, DynamoDB tables, and ElastiCache clusters. | 16/10/2026 | 16/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://docs.aws.amazon.com/dynamodb/> |

### Week 5 Achievements:

* Mastered selection criteria across Amazon RDS/Aurora, Amazon DynamoDB, and Amazon ElastiCache.
* Executed DynamoDB CRUD, Query/Scan, and GSI workflows across both AWS Console and CloudShell/Boto3.
* Wired a web application securely to S3 and DynamoDB via IAM Roles, published Blogs 1 & 3, and cleaned up all test databases.
