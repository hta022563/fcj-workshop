---
title: "Week 10: 60 FPS Dynamic Watermark, AI Anomaly Dashboard & Leak Tracing"
date: 2026-11-16
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Implement a continuously moving Dynamic Watermark overlay inside the video player to deter and trace unauthorized screen recordings.
* Build the Administrator Portal suite: AI Anomaly Dashboard (AdminAnomalyDashboard), Leak Tracing (LeakTracing), User Management, and System Config.
* Coordinate AI access-log schema consumption from the Isolation Forest / EventBridge / SNS pipeline onto the Admin UI.
* Finalize Blogs (Blogs 1–3), Proposal, and Events Participated sections on the internship report site.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Build custom hook useDynamicWatermark using requestAnimationFrame (60 FPS) to animate a bouncing edge-collision watermark (DVD screensaver pattern). <br> - Render Student ID alongside a per-second live timestamp with randomized angle and bounce velocity perturbations to prevent static cropping. <br> - Integrate the hook into the playback experience and profile rendering smoothness alongside active HLS decoding. | 16/11/2026 | 16/11/2026 | <https://000056.awsfcaj.com/> <br> <https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame> |
| Tue | - Build AdminAnomalyDashboard consuming real Backend logs (/api/v1/ai/logs) and Cognito user records via adminService.js. <br> - Implement buildAnomalyAlertsFromLogs grouping user logs by email to highlight multi-IP access, multi-device fingerprints, key/manifest bursts, errors, and rapid scrubbing. <br> - Add search filters, anomaly resolution tracking in localStorage, and detailed incident inspection drawers. | 17/11/2026 | 17/11/2026 | <https://000200.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Wed | - Build the LeakTracing console enabling admins to look up leaked watermark IDs, inspect course entitlements/sessions, and suspend offending accounts. <br> - Implement AdminUserManagement wired to Cognito user CRUD endpoints (GET / POST / DELETE /admin/user). <br> - Deliver AdminSystemConfig calculating storage footprint, access-log counts, estimated cloud cost, AI scoring thresholds, and KMS key rotation settings. | 18/11/2026 | 18/11/2026 | <https://docs.aws.amazon.com/cognito/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Thu | - Collaborate on the AI Branch Flow architecture (Access Logs → CloudWatch/DynamoDB → 5-min EventBridge → Isolation Forest Lambda .pkl on R2 → Amazon SNS). <br> - Align frontend anomaly dashboard metrics with alerts dispatched via Amazon SNS emails. <br> - Study asynchronous fan-out and queuing patterns across Amazon SQS and Amazon SNS. | 19/11/2026 | 19/11/2026 | <https://000077.awsfcaj.com/> <br> <https://000083.awsfcaj.com/> |
| Fri | - Publish Blogs 1, 2, and 3, Proposal updates, and Events Participated entries across the Hugo report. <br> - End-to-end test Admin Portal flows: Cognito user provisioning, anomaly log inspection, and watermark leak lookup. <br> - Sync 10-week progress across Coursera, FCJ Portal, and SAA-C03 curricula. | 20/11/2026 | 20/11/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://cloudjourney.awsfcaj.com/> |

### Week 10 Achievements:

* Delivered the 60 FPS Dynamic Watermark engine (useDynamicWatermark) supporting live leak attribution on the player.
* Completed the full Admin Portal suite covering AdminAnomalyDashboard, LeakTracing, AdminUserManagement, and AdminSystemConfig.
* Published Blogs 1–3, Events Participated, and aligned frontend anomaly telemetry with backend AI monitoring.
