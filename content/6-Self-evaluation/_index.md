---
title: "Self-Assessment"
date: 2026-11-20
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Wrapping up the **Workforce Bootcamp – First Cloud AI Journey (FCAJ)** internship at **Amazon Web Services Viet Nam Company Limited** (14/09/2026 – 14/12/2026), my biggest takeaway isn't that I suddenly became a cloud expert, but that I stopped feeling intimidated by real systems and learned to work with much better discipline.

In the first couple of weeks, opening the AWS Console genuinely made me nervous. There were so many services, and I kept worrying one wrong click would leave a surprise bill. That worry actually taught me good habits early: enabling MFA on the root account, sticking to IAM users/roles, and setting up a 12.5% AWS Budgets alert before touching VPC or EC2. Going to the in-person sessions at Bitexco Tower also made cloud engineering feel much more down-to-earth than classroom slides.

Once we started **SecureLearn** in Week 7, I took on **Frontend development and helped shape the system architecture**. Things got real pretty fast: there were late nights figuring out why HLS.js wasn't loading AES-128 keys properly, and tweaking the 60 FPS Dynamic Watermark so it wouldn't drift in Fullscreen mode. Near the end, after sending our architecture diagram over WhatsApp and receiving feedback from Mr. Hung and our mentors, we pivoted the whole stack onto AWS (S3, CloudFront, WAF, ECS Fargate, RDS), which meant rushing to adjust the FE config and retest everything. It was tiring, but seeing the screen black out immediately on PrintScreen, watching real logs show up on AdminAnomalyDashboard, and tracing a watermark in LeakTracing made all the debugging worth it.

Looking back honestly, I still have clear gaps to work on. Here is my candid self-evaluation across the three months:

| No. | Criteria | Description | Good | Fair | Average |
| --- | --- | --- | --- | --- | --- |
| 1 | **Professional knowledge & skills** | Cloud/Frontend understanding, applying it in SecureLearn, output quality | ☐ | ✅ | ☐ |
| 2 | **Ability to learn** | Picking up new tools (AWS services, HLS.js, CloudFront SPA deployment) | ✅ | ☐ | ☐ |
| 3 | **Proactiveness** | Reading docs independently and taking ownership of FE & architecture work | ✅ | ☐ | ☐ |
| 4 | **Sense of responsibility** | Following through on assigned features ahead of demo milestones | ✅ | ☐ | ☐ |
| 5 | **Time management & Discipline** | Balancing coding, testing, and documentation deadlines | ☐ | ☐ | ✅ |
| 6 | **Progressive mindset** | Acting on feedback from mentors, Mr. Hung, and teammates | ✅ | ☐ | ☐ |
| 7 | **Communication & Presentation** | Explaining technical ideas clearly and speaking confidently in reviews | ☐ | ☐ | ✅ |
| 8 | **Teamwork** | Coordinating smoothly between React FE and Backend/Cloud teammates | ✅ | ☐ | ☐ |
| 9 | **Professional conduct** | Respecting teammates, mentors, and workplace guidelines | ✅ | ☐ | ☐ |
| 10 | **Problem-solving skills** | Debugging CORS, HLS playback, and role-based access issues | ☐ | ✅ | ☐ |
| 11 | **Contribution to project/team** | Building all three FE portals, anti-capture guards, and data-flow designs | ☐ | ✅ | ☐ |
| 12 | **Overall** | Honest overall rating for the internship | ☐ | ✅ | ☐ |

### What Went Well

* **Seeing beyond just the UI:** Before this internship, I mostly built React apps running on localhost. Now I understand how requests travel through CloudFront, WAF, and ALB into the backend, why a CloudFront Function is needed for SPA routing, and where JWTs and Device Fingerprints fit in.
* **Shipping real client-side security:** Building the player hooks (useSecureHls, useSecurePlayer, useDynamicWatermark, useVideoVisibility) made the frontend an actual part of the anti-piracy defense rather than just visuals.
* **Pulling together with the team:** Even when we had to pivot to an all-AWS architecture late in the schedule, we stayed focused, rewired the frontend, retested the flows, and got the demo done.

### What I Still Need to Improve

* **Communication & presenting (Average):** I still get nervous when explaining architectural choices to mentors. Sometimes I understand the issue in my head, yet ramble instead of stating the point directly. I need to practice keeping explanations short and asking questions earlier instead of getting stuck alone.
* **Time management (Average):** A few times I got carried away polishing React animations and minor UI details, leaving documentation and regression checks tighter than they should have been. I need to lock down core flows first before fine-tuning visuals.
* **Hands-on Backend/DevOps depth (Fair):** I understand how our ECS, RDS, and Lambda pieces fit together, though my own hands-on fluency operating production infrastructure still needs work. Next, I plan to build more end-to-end AWS labs and keep studying for the AWS Solutions Architect – Associate (SAA-C03) exam.
