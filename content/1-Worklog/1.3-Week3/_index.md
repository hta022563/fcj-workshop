---
title: "Week 3: AWS Networking, Amazon VPC & Route 53"
date: 2026-09-28
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Understand foundational AWS Networking components: VPC, CIDR, Subnets, Route Tables, ENI, Internet Gateway, and NAT Gateway.
* Configure layered network security using stateful Security Groups and stateless Network ACLs.
* Practice private connectivity and multi-network topologies: Session Manager, VPC Endpoints, VPC Peering, Transit Gateway, and Route 53 DNS.
* Debug common VPC routing errors and perform full cleanup of temporary networking assets.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Learn core AWS Networking components: Region, AZ, VPC, Subnet, Route Table, ENI, EIP, IGW, NAT Gateway, Security Group, and NACL. <br> - Plan non-overlapping CIDR blocks and segment multi-AZ Public and Private Subnets. | 28/09/2026 | 28/09/2026 | <https://000003.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| Tue | - Configure Route Tables routing Public Subnets to an Internet Gateway and Private Subnets through a NAT Gateway. <br> - Study Route 53 DNS, Internal Hosted Zones, DNS Endpoints, and AWS Global Accelerator. <br> - Practice configuring basic DNS routing records on Route 53. | 29/09/2026 | 29/09/2026 | <https://000010.awsfcaj.com/> <br> <https://000092.awsfcaj.com/> |
| Wed | - Study VPC Endpoints (Gateway & Interface Endpoints) to connect AWS services over private networks. <br> - Practice connecting to Private Subnet EC2 instances via Systems Manager Session Manager without opening SSH port 22. <br> - Explore multi-VPC patterns: VPC Peering, Transit Gateway, and Site-to-Site VPN. | 30/09/2026 | 30/09/2026 | <https://000058.awsfcaj.com/> <br> <https://000111.awsfcaj.com/> |
| Thu | - Build a custom VPC from scratch with Subnets, IGW, Route Tables, and Security Group / NACL rules. <br> - Deploy a sample web application inside the new VPC and test connectivity between web and data tiers. <br> - Verify allow/deny behavior across stateful Security Groups and stateless NACLs. | 01/10/2026 | 01/10/2026 | <https://000020.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Fri | - Practice diagnosing common VPC issues (missing 0.0.0.0/0 routes, asymmetric NACL inbound/outbound rules). <br> - Complete Module 2 assessment on Coursera and publish the Event 1 reflection (4.1-Event1). <br> - Clean up temporary VPCs, NAT Gateways, Elastic IPs, and test networking resources. | 02/10/2026 | 02/10/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/vpc-troubleshooting.html> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |

### Week 3 Achievements:

* Built multi-AZ Amazon VPC architectures complete with Public/Private Subnets, IGW, NAT Gateway, and Route Tables.
* Adopted Session Manager and VPC Endpoints to keep internal servers and traffic off the public Internet.
* Understood Route 53, VPC Peering, Transit Gateway, and executed clean teardown of billed networking components.
