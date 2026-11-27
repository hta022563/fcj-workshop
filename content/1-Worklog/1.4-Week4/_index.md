---
title: "Week 4: AWS Storage Services (EBS, EFS, S3 & CloudFront)"
date: 2026-10-05
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Distinguish Block Storage (Instance Store, Amazon EBS), File Storage (Amazon EFS, FSx), and Object Storage (Amazon S3).
* Practice creating and securing Amazon S3 buckets (Block Public Access, Bucket Policies, Encryption, Presigned URLs, Lifecycle Rules).
* Automate EBS snapshots, review centralized AWS Backup, and deliver content globally via Amazon CloudFront.
* Finalize Blog 2 on Zero Trust & Least Privilege and clean up test storage assets.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Learn the three AWS storage families (Block, File, Object) and selection criteria by IOPS and latency. <br> - Explore S3 Buckets, Object Keys, 11-nines durability (99.999999999%), and S3 Storage Classes. <br> - Study automated Lifecycle transition rules and Cross-Region Replication. | 05/10/2026 | 05/10/2026 | <https://000068.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Tue | - Contrast ephemeral EC2 Instance Store with persistent Amazon EBS (gp3, io2) and shared multi-AZ Amazon EFS / FSx. <br> - Practice automated snapshot scheduling and retention using EBS Data Lifecycle Manager. <br> - Explore centralized backup governance with AWS Backup. | 06/10/2026 | 06/10/2026 | <https://000088.awsfcaj.com/> <br> <https://000013.awsfcaj.com/> |
| Wed | - Create an Amazon S3 bucket on Console, enable Versioning, and test Static Website Hosting. <br> - Practice aws s3 cp and aws s3 sync commands via AWS CLI and CloudShell. <br> - Verify object recovery from delete markers when S3 Versioning is active. | 07/10/2026 | 07/10/2026 | <https://000057.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| Thu | - Harden S3 security: enable Block Public Access, author Bucket Policies, and configure SSE-S3 / SSE-KMS encryption. <br> - Test time-bounded Presigned URLs for private object downloads. <br> - Deploy a CloudFront Distribution backed by S3 Origin Access Control (OAC) for private edge delivery. | 08/10/2026 | 08/10/2026 | <https://000069.awsfcaj.com/> <br> <https://000094.awsfcaj.com/> |
| Fri | - Evaluate cost-optimal storage tiering strategies by access frequency. <br> - Finalize and publish **Blog 2** (*AWS Security: Zero Trust & Least Privilege*). <br> - Clean up temporary S3 buckets, CloudFront distributions, and EBS snapshots. | 09/10/2026 | 09/10/2026 | <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://docs.aws.amazon.com/s3/> |

### Week 4 Achievements:

* Mastered selection criteria and performance characteristics across Instance Store, EBS, EFS, S3, and CloudFront.
* Configured locked-down S3 buckets, Presigned URLs, and CloudFront OAC distributions.
* Applied Lifecycle Rules and snapshot automation, published Blog 2, and cleaned up all lab resources.
