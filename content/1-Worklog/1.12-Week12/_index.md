---
title: "Week 12: Final Slides, Report QA & AWS Resource Cleanup"
date: 2026-11-20
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Finish the SecureLearn defense slide deck reflecting the revised AWS architecture.
* Do a final read-through of the bilingual internship report (through the 30/11/2026 cutoff) to catch any broken links, images, or typos.
* Review core SAA-C03 topics and clean up all temporary AWS resources after demo recording.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Finished the defense slides covering the updated AWS architecture (refined with mentors and Mr. Hung), Frontend player security (HLS.js, Dynamic Watermark, anti-capture), and cost estimates. <br> - Audited every bilingual page on the Hugo report site (Worklog, Proposal, Blogs, Events, Workshop, Self-Evaluation, Feedback), verifying all links and screenshots as of 30/11/2026. <br> - Reviewed key Q&A topics around VPCs, the CloudFront → ALB → ECS → RDS security group chain, Cognito, and WAF. <br> - Helped tear down AWS resources in priority order: stopped ECS, ALB, and RDS first to avoid hourly charges, then deleted CloudFront, WAF, S3, ECR, Lambda, DynamoDB, SNS, EventBridge, KMS (scheduled), and CloudWatch Logs. | 30/11/2026 | 30/11/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://cloudjourney.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://docs.aws.amazon.com/cost-management/latest/userguide/ce-delete-budget.html> |

### Week 12 Achievements:

* Completed the presentation slides and bilingual internship report cleanly on 30/11/2026.
* Consolidated 12 weeks of AWS learning and prepared for defense Q&A.
* Cleaned up all hourly and storage AWS resources with no stray charges left behind.
