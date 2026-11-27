---
title: "Week 2: AWS Compute Services (EC2, Containers & Serverless)"
date: 2026-09-21
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Understand AWS compute paradigms spanning virtual machines (EC2), containers (ECS/EKS/Fargate), and serverless (AWS Lambda).
* Practice launching EC2 instances, managing lifecycle states, connecting over SSH, attaching EBS volumes, and assigning IAM Instance Profiles.
* Evaluate resource footprint and licensing trade-offs between Amazon Linux 2023 and Windows Server AMIs.
* Attend the Buildrathon Kickoff event to explore Generative AI and AI Agent trends.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Study Compute as a Service concepts, EC2 instance families, and vCPU/memory sizing strategies. <br> - Compare EC2 pricing options: On-Demand, Reserved Instances, Spot Instances, and Savings Plans. <br> - Understand how Amazon Machine Images (AMIs) package operating systems and runtime templates. | 21/09/2026 | 21/09/2026 | <https://000004.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| Tue | - Learn EC2 Instance Lifecycle states (Pending, Running, Stopping, Stopped, Terminated) and Elastic IPs. <br> - Launch an Amazon Linux 2023 EC2 instance, create a Key Pair, and establish an SSH session. <br> - Attach an additional EBS volume and bind an IAM Instance Profile instead of storing static credentials. | 22/09/2026 | 22/09/2026 | <https://000048.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Wed | - Study Docker packaging basics and AWS container services: Amazon ECR, Amazon ECS, and Amazon EKS. <br> - Deploy serverless containers without managing underlying hosts using AWS Fargate. <br> - Compare operational overhead and flexibility between standard EC2 deployments and Fargate tasks. | 23/09/2026 | 23/09/2026 | <https://000015.awsfcaj.com/> <br> <https://000067.awsfcaj.com/> |
| Thu | - Learn event-driven AWS Lambda fundamentals, execution roles, timeouts, and memory allocation. <br> - Author a Lambda function handling test JSON payloads, inspect execution logs, and review per-invocation billing. <br> - Contrast Amazon Linux 2023 vs. Windows Server AMIs to prepare materials for Blog 3. | 24/09/2026 | 24/09/2026 | <https://000022.awsfcaj.com/> <br> <https://docs.aws.amazon.com/linux/al2023/ug/what-is-amazon-linux.html> |
| Fri | - Review EC2 Right-Sizing optimization techniques and inspect active compute allocations. <br> - Terminate temporary EC2 instances, detach/delete unused EBS volumes, and clean up lab assets. <br> - Prepare and attend the Buildrathon Kickoff event with CMC Global (26/09/2026). | 25/09/2026 | 25/09/2026 | <https://000032.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Week 2 Achievements:

* Provisioned EC2 instances with SSH access, EBS storage attachments, and IAM Instance Profiles safely.
* Understood clear selection criteria across EC2, ECS/EKS on Fargate, and AWS Lambda by workload pattern.
* Analyzed cost and resource trade-offs between Linux and Windows AMIs and cleaned up all temporary resources.
