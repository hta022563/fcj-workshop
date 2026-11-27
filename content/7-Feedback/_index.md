---
title: "Sharing and Feedback"
date: 2026-11-20
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### What Changed Most Over These Three Months

Before joining the **Workforce Bootcamp – First Cloud AI Journey (FCAJ)** program at **Amazon Web Services Viet Nam Company Limited** (14/09/2026 – 14/12/2026), my approach to school projects was pretty simple: build the React UI, wire up an API on localhost, and call it finished. Three months with cohort AWS082025, especially working on **Frontend and system architecture** for **SecureLearn**, changed how I think about building software.

Working on a real cloud deployment showed me that getting features to run is only half the story; the rest is security, cost, and how services actually talk to one another. Even a single playback flow in SecureLearn involved tracing Cognito JWTs, browser Device Fingerprints, CloudFront and AWS WAF routing into Spring Boot on ECS Fargate, AES-128 keys, 60-second S3 presigned segments, plus the 60 FPS Dynamic Watermark and anti-PrintScreen guards in the browser. After sending our architecture diagram on WhatsApp and getting feedback from Mr. Hung and our mentors, consolidating our initial draft onto an all-AWS stack made the architecture much cleaner. It also taught me practical cost habits, like shutting down ECS and RDS outside working hours to bring monthly costs from ~$165 down to roughly ~$60–75.

### What Stood Out About the FCAJ Community

Aside from studying through Coursera, First Cloud Journey labs, and the SAA-C03 course, my favorite memories were the in-person sessions on the 26th floor of Bitexco Tower. Hearing engineers from AWS, CMC Global, STYL Solutions, CloudThinker, and NAB talk honestly about real production mistakes (like Serverless cost traps, or AI prototypes that work locally but break in production) gave an FPT University IT student like me a much clearer picture of what skills matter next.

Working closely with my SecureLearn teammates was just as memorable, from chasing down stubborn CORS bugs to cleaning up AWS resources together at the end. The approachable vibe from both mentors and classmates made it much easier to speak up and ask questions.

### A Few Suggestions for Future Cohorts

Speaking from the perspective of someone focusing on Frontend while learning Cloud architecture, I have four small suggestions for upcoming cohorts:

* **Add a short Frontend-to-AWS integration lab:** Most labs focus on the AWS Console or CLI. A quick guide showing how a real React/SPA app connects to Cognito, uses a CloudFront Function for SPA routes, and uploads large files via S3 Presigned URLs would save Frontend-focused interns a lot of trial and error during capstone projects.
* **Hold quick architecture check-ins around Weeks 7–8:** Sending our diagram over WhatsApp to Mr. Hung and the mentors gave us super helpful feedback, so having an early review checkpoint right after teams draft their Proposal would help catch things like CloudFront's 60-second timeout or ECS/RDS hourly costs early before heavy coding starts.
* **Mix in a few break-and-fix troubleshooting exercises:** Adding occasional intentional misconfigurations (missing IAM permissions, CORS headers, expired tokens) alongside step-by-step labs would help interns get comfortable reading CloudWatch logs and diagnosing issues faster.
* **Adjust the office AC temperature in the afternoon:** From around 2:30 PM onward, the room suddenly gets freezing cold from the floor up, to the point where even wearing a jacket barely helps and forgetting one makes it really tough to focus. Raising the AC temperature a bit in the afternoon would make the workspace much more comfortable for future cohorts.

### Thank You

Finally, thank you to the FCAJ organizers, Mr. Hung, all the mentors, guest speakers, cohort AWS082025, and my SecureLearn teammates for a supportive and memorable three months. Moving forward, I plan to keep studying for the AWS Solutions Architect – Associate (SAA-C03) certification and continue growing across both Frontend engineering and Cloud Architecture.
