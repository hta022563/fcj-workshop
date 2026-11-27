---
title: "Week 11: Moving Architecture to AWS, FE Polish & Demo Recording"
date: 2026-11-20
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Update the project architecture to an all-AWS setup based on feedback from mentors and Mr. Hung.
* Deploy the React Frontend build to Amazon S3 + CloudFront with SPA routing and AWS WAF protection.
* Retest secure playback, client-side defenses, and the updated AI v2 pipeline on AWS.
* Record the demo video and align Proposal, Blogs, and Workshop docs with the team.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Sent our architecture diagram to Mr. Hung and the mentors on WhatsApp for review; based on their feedback, our team agreed to move the whole stack onto AWS (ECS Fargate, ALB, RDS, private S3, CloudFront, AWS WAF) for cleaner IAM and security boundaries. <br> - Updated FE .env.production to use VITE_API_URL=/api/v1 so frontend and API share one CloudFront domain without CORS headaches. | 23/11/2026 | 23/11/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html> <br> <https://000080.awsfcaj.com/> |
| Tue | - Built the React bundle (npm run build), synced to S3 securelearn-web with CloudFront OAC, and added CloudFront Function securelearn so SPA routes do not 404 on refresh. <br> - Fixed remaining UI glitches, verified Fullscreen Dynamic Watermark alignment, and checked AdminAnomalyDashboard data. | 24/11/2026 | 24/11/2026 | <https://github.com/video-dev/hls.js/> <br> <https://www.framer.com/motion/> |
| Wed | - Tested direct S3 uploads (SSE-KMS), 60-second presigned AES-128 HLS segments, and tried Apple HLS AES-128 static-key output on MediaConvert. <br> - Verified security checks: AWS WAF blocking admin APIs outside the IP allowlist, direct ALB calls returning 403, and browser anti-PrintScreen / tab-blur blackout. | 25/11/2026 | 25/11/2026 | <https://000098.awsfcaj.com/> <br> <https://000018.awsfcaj.com/> <br> <https://000085.awsfcaj.com/> |
| Thu | - Tested the AI v2 pipeline with the team: DynamoDB AccessLog Stream (with byUserTime GSI) invoking the ECR Lambda running isolation_forest_securelearn_v2.pkl, sending SNS alerts, and verifying optional Cognito lockout on a test user. <br> - Reviewed updated costs in AWS Cost Explorer (~$165/month running 24/7, or ~$60–75/month shutting down ECS/RDS off-hours). | 26/11/2026 | 26/11/2026 | <https://000074.awsfcaj.com/> <br> <https://000064.awsfcaj.com/> <br> <https://000140.awsfcaj.com/> |
| Fri | - Recorded and edited the 5–7 minute demo video covering all flows on the new AWS deployment. <br> - Synced the three group sections (Proposal, Blogs, and AWS Workshop) on our Hugo report site to match the revised architecture. | 27/11/2026 | 27/11/2026 | <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://vitejs.dev/guide/build.html> |

### Week 11 Achievements:

* Completed the transition to an all-AWS architecture per mentor and Mr. Hung's feedback, with the React FE running smoothly on S3 + CloudFront + WAF.
* Verified security layers end to end, from WAF, OAC, and 60s presigned URLs to browser watermark/blackout and AI v2 alerts.
* Finished the demo video and synced all group documentation on the report site.
