---
title: "Week 9: Secure HLS Player, Key/Manifest Decryption & Client-Side Defenses"
date: 2026-11-09
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Integrate HLS.js with a Custom Loader to fetch short-lived signed manifests and AES-128 decryption keys from the Backend.
* Engineer client-side anti-capture, focus-loss blackout, and DevTools deterrence layers inside the learner player.
* Complete StudentCoursePlayer, InstructorVideoPreview, and end-to-end Playback Flow integration.
* Review edge defense architecture (WAF/Shield, Signed URLs, Zero Trust Access) and validate segment playback security.

### Tasks Carried Out This Week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Build playbackService.js and cryptoService.js calling /api/v1/lesson/{id}/playback with UUID validation and structured 401/403/404 handling. <br> - Implement useSecureHls with HLS.js and a custom SecureKeyFragmentLoader intercepting manifest and key requests. <br> - Inject Bearer JWT and X-Device-Fingerprint on .m3u8 manifest and AES-128 key loads, plus Safari Native HLS fallback. | 09/11/2026 | 09/11/2026 | <https://github.com/video-dev/hls.js/> <br> <https://000141.awsfcaj.com/> |
| Tue | - Build SecureVideoPlayer wrapping HTML5 video with nodownload, disablePictureInPicture, and blocked right-click context menus. <br> - Implement useSecurePlayer enforcing Focus-based Blackout (instant black overlay + pause on blur/Snipping Tool), Anti-PrintScreen, and DevTools shortcut blocking. <br> - Overwrite clipboard contents with a copyright notice and force a 3.5-second blackout curtain whenever PrintScreen is triggered. | 10/11/2026 | 10/11/2026 | <https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| Wed | - Implement useVideoVisibility using the Page Visibility API to detect background tab switches while playing (BACKGROUND_PLAY). <br> - Pause playback automatically on tab hide, raise a focus warning overlay, and require manual resume upon return. <br> - Co-test short-lived Signed Playback URLs and HMAC token expiration (< 1 hour) with Backend services. | 11/11/2026 | 11/11/2026 | <https://000033.awsfcaj.com/> <br> <https://developer.mozilla.org/en-US/docs/Web/API/Page_Visibility_API> |
| Thu | - Finalize StudentCoursePlayer, UserProfile, UserPortal, and InstructorVideoPreview screens. <br> - Review perimeter security architecture including Cloudflare Zero Trust Access for admin paths and Cognito JWT boundaries. <br> - Build the internal DbExplorer developer view to inspect mock entity schemas and playback states during integration. | 12/11/2026 | 12/11/2026 | <https://000133.awsfcaj.com/> <br> <https://developers.cloudflare.com/cloudflare-one/> |
| Fri | - Review Layer-7 and DDoS defense patterns across AWS WAF, AWS Shield, and Cloudflare WAF shielding API Gateway and CDN edges. <br> - Run end-to-end Playback Flow integration tests: Cognito JWT → Entitlement Check → Signed Manifest → AES-128 Key → SecureVideoPlayer. <br> - Verify HTTP 403 rejections for unenrolled students or requests missing valid fingerprints/tokens. | 13/11/2026 | 13/11/2026 | <https://000026.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Week 9 Achievements:

* Shipped SecureVideoPlayer powered by useSecureHls (Custom Key Loader), useSecurePlayer (Anti-PrintScreen/Focus Blackout), and useVideoVisibility.
* Verified end-to-end encrypted HLS AES-128 playback and strict 401/403 authorization enforcement from browser to backend.
* Delivered StudentCoursePlayer and InstructorVideoPreview workspaces for learner and instructor playback verification.
