---
title: "Week 7: SecureLearn Architecture, UI/UX Design & React Frontend Setup"
date: 2026-10-26
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Design the end-to-end Hybrid Serverless (AWS + Cloudflare) architecture for SecureLearn, defining clear boundaries between Control Plane, Media Plane, and Frontend Client.
* Study HLS stream protection patterns, AWS KMS / Secrets Manager custody, and validate the design against all 6 AWS Well-Architected pillars.
* Bootstrap the ReactJS + Vite + TailwindCSS frontend codebase with bilingual i18n support and role-based portal routing.
* Finalize the bilingual Proposal and attend AWS First Cloud AI Journey Community Day 2026.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Analyze lecture video piracy risks in SME education platforms and commercial DRM cost barriers. <br> - Lock down In-Scope boundaries (HLS/AES-128, JWT, short-lived playback tokens, Device Fingerprint, Dynamic Watermark, AI anomaly alerts) and Out-of-Scope items. <br> - Align on the Event-Driven architecture connecting the React frontend, API Gateway/Lambda, and Cloudflare R2. | 26/10/2026 | 26/10/2026 | <https://000054.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Tue | - Study AWS Elemental MediaConvert, Cloudflare R2 S3-API compatibility (Zero Egress Fee), and HLS AES-128 encryption concepts. <br> - Review AWS KMS (CMK) and Secrets Manager key custody patterns across the Control Plane and Media Plane. <br> - Define shared REST API contracts between Frontend and Backend for auth, upload, and secure playback endpoints. | 27/10/2026 | 27/10/2026 | <https://000033.awsfcaj.com/> <br> <https://000096.awsfcaj.com/> |
| Wed | - Author the three system data-flow diagrams: Upload Flow, Playback Flow, and AI Branch Flow. <br> - Evaluate the SecureLearn architecture across all 6 AWS Well-Architected Framework pillars. <br> - Build the monthly cost estimate (~$46–$48.60 USD/month) and Risk Assessment Matrix. | 28/10/2026 | 28/10/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| Thu | - Initialize the React 18 + Vite 5.4 + TailwindCSS 3.4 + Framer Motion + Lucide Icons client application. <br> - Implement core UI foundation layers: ThemeContext (Dark/Light Mode), ToastProvider, MeshGradientBackground, ParticleBackground, and ErrorBoundary. <br> - Configure Vietnamese/English localization via i18next / react-i18next with LayoutWithLanguage and LanguageSwitcher. | 29/10/2026 | 29/10/2026 | <https://react.dev/> <br> <https://tailwindcss.com/docs> |
| Fri | - Architect role-aware routing in App.jsx using ProtectedRoute for Student, Instructor, and Administrator portals driven by JWT claims. <br> - Implement RolePortalLayout, MainNavbar, and finalize the bilingual Proposal page. <br> - Attend AWS First Cloud AI Journey Community Day 2026 (31/10/2026) at Bitexco Financial Tower. | 30/10/2026 | 31/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://reactrouter.com/> |

### Week 7 Achievements:

* Finalized SecureLearn's Well-Architected architecture blueprint, three core data-flow diagrams, and FE–BE API contracts.
* Scaffolded the React + TailwindCSS frontend supporting Dark Mode, bilingual i18next localization, and role-isolated portals.
* Delivered the bilingual Proposal document and brought back practical Cloud/AI insights from Community Day.
