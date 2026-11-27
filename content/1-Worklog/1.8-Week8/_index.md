---
title: "Week 8: Frontend Cognito Auth, Device Fingerprinting & Video Upload Flow"
date: 2026-11-02
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Build core public catalog views (Home, Course Catalog, Subject Lectures) and Cognito JWT login/registration flows.
* Implement browser-based Device Fingerprinting on the client side to reinforce session binding and anti-sharing telemetry.
* Build the instructor lecture upload pipeline pushing files directly to Cloudflare R2 via Presigned URLs.
* Integration-test Frontend services against the Backend APIs (Spring Boot and AWS API Gateway).

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Build Home (with HeroStatsCard, LearningTimeline), CourseCatalog, SubjectLectures, and MyCourses views. <br> - Implement courseService.js, subjectService.js, and entitlementService.js for catalog queries and enrollment validation. <br> - Create CreateCourseModal and CreateSubjectModal workflows for content organization. | 02/11/2026 | 02/11/2026 | <https://000078.awsfcaj.com/> <br> <https://react.dev/> |
| Tue | - Develop authentication pages and components: Login, Register, OtpInput (Cognito confirmation), and ForgotPasswordModal. <br> - Wire AuthContext with sessionStorage persistence and authService.js (register, login, token refresh, global logout). <br> - Configure Axios interceptors in axiosClient.js to attach Bearer JWT headers across protected requests. | 03/11/2026 | 03/11/2026 | <https://000081.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Wed | - Integrate @fingerprintjs/fingerprintjs in fingerprintService.js to extract real browser visitorId hardware/environment signals. <br> - Implement a Web Crypto SHA-256 fallback digest (userAgent, language, screen size, timezone) when FingerprintJS is blocked. <br> - Cache device_fingerprint in sessionStorage and inject X-Device-Fingerprint headers on auth and playback requests. | 04/11/2026 | 04/11/2026 | <https://github.com/fingerprintjs/fingerprintjs> <br> <https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto> |
| Thu | - Build instructor portal views: InstructorVideos, UploadVideo, and ReuploadVideoModal. <br> - Implement useVideoUpload and uploadService.js handling the 3-stage pipeline: request Presigned URL, PUT directly to R2, and trigger /upload/process HLS transcoding. <br> - Track live byte upload percentages across lifecycle states (uploading, processing, ready, error) with unmount safety guards. | 05/11/2026 | 05/11/2026 | <https://000137.awsfcaj.com/> <br> <https://developers.cloudflare.com/r2/> |
| Fri | - Co-test the full Upload Flow with Backend: UploadVideo → R2 Presigned Upload → HLS Transcoding → Lesson Catalog refresh. <br> - Validate error handling, interrupted uploads, and Instructor ProtectedRoute access guards. <br> - Align upload payload schemas with AWS API Gateway and Lambda webhook specifications. | 06/11/2026 | 06/11/2026 | <https://000066.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Week 8 Achievements:

* Delivered Home, Catalog, Cognito OTP authentication flows, and AuthContext + Axios JWT integration.
* Shipped real browser fingerprinting via fingerprintService.js feeding X-Device-Fingerprint telemetry.
* Verified direct-to-R2 presigned video uploads with live byte progress in the Instructor portal.
