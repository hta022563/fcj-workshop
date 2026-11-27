---
title: "Tuần 9: Trình phát HLS Bảo mật, Mã hóa Key/Manifest & Phòng thủ Client-side"
date: 2026-11-09
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Tích hợp thư viện HLS.js kèm Custom Loader để tải manifest được ký và khóa giải mã AES-128 an toàn từ Backend.
* Xây dựng các lớp bảo vệ chống chụp/quay màn hình, chống mất tập trung và hạn chế mở DevTools ngay trên trình duyệt học viên.
* Hoàn thiện giao diện xem bài giảng StudentCoursePlayer, xem trước giảng viên InstructorVideoPreview và luồng Playback Flow.
* Phối hợp rà soát kiến trúc bảo mật lớp biên (WAF/Shield, Signed URL, Zero Trust Access) và kiểm thử phát video đa phân đoạn.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Phát triển playbackService.js và cryptoService.js gọi API lấy đường dẫn phát bảo mật (/api/v1/lesson/{id}/playback) kèm kiểm tra UUID và xử lý các mã lỗi 401/403/404. <br> - Xây dựng custom hook useSecureHls kết hợp HLS.js và lớp SecureKeyFragmentLoader tùy biến để can thiệp từng request tải key/fragment. <br> - Đính kèm Bearer JWT và X-Device-Fingerprint khi tải manifest .m3u8 và khóa giải mã AES-128, hỗ trợ fallback Native HLS trên Safari. | 09/11/2026 | 09/11/2026 | <https://github.com/video-dev/hls.js/> <br> <https://000141.awsfcaj.com/> |
| 3 | - Thiết kế component SecureVideoPlayer tích hợp thẻ video HTML5 (nodownload, disablePictureInPicture, chặn chuột phải onContextMenu). <br> - Xây dựng custom hook useSecurePlayer triển khai 3 lớp bảo vệ: Focus-based Blackout (phủ đen & dừng phát khi blur hoặc mở Snipping Tool), Anti-PrintScreen và chặn phím tắt DevTools / View Source. <br> - Cài đặt cơ chế ghi đè Clipboard thông báo bản quyền và phủ đen cưỡng chế trong 3.5 giây khi phát hiện phím PrintScreen. | 10/11/2026 | 10/11/2026 | <https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 4 | - Lập trình hook useVideoVisibility sử dụng Page Visibility API phát hiện học viên chuyển tab khi video đang phát (sự kiện BACKGROUND_PLAY). <br> - Tự động tạm dừng video ngay khi ẩn tab, hiển thị overlay cảnh báo tập trung và không tự phát lại khi học viên quay về. <br> - Kết hợp với Backend kiểm thử vòng đời Signed Playback URL / HMAC token có thời hạn ngắn (< 1 giờ). | 11/11/2026 | 11/11/2026 | <https://000033.awsfcaj.com/> <br> <https://developer.mozilla.org/en-US/docs/Web/API/Page_Visibility_API> |
| 5 | - Hoàn thiện trang học viên StudentCoursePlayer, hồ sơ UserProfile, cổng UserPortal và trang xem trước InstructorVideoPreview. <br> - Rà soát kiến trúc bảo vệ phân quyền: khóa cổng quản trị qua Cloudflare Zero Trust, ranh giới truy cập Cognito JWT và nguyên tắc Least Privilege IAM. <br> - Xây dựng công cụ phát triển DbExplorer hỗ trợ đội ngũ kiểm tra dữ liệu và cấu trúc thực thể trong quá trình tích hợp. | 12/11/2026 | 12/11/2026 | <https://000133.awsfcaj.com/> <br> <https://developers.cloudflare.com/cloudflare-one/> |
| 6 | - Tham khảo mô hình phòng thủ lớp ứng dụng bằng AWS WAF, AWS Shield và Cloudflare WAF bảo vệ API Gateway / CDN. <br> - Phối hợp kiểm thử đầu-cuối Playback Flow: xác thực JWT → kiểm tra Entitlement → tải Manifest đã ký → giải mã AES-128 phát trên SecureVideoPlayer. <br> - Xác nhận từ chối HTTP 403 đối với tài khoản chưa ghi danh khóa học hoặc request thiếu fingerprint/token hợp lệ. | 13/11/2026 | 13/11/2026 | <https://000026.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Kết quả đạt được tuần 9:

* Hoàn thiện trình phát SecureVideoPlayer với useSecureHls (Custom Key Loader), useSecurePlayer (chống PrintScreen/blur blackout) và useVideoVisibility.
* Tích hợp trơn tru Playback Flow bảo mật từ Backend xuống trình duyệt, hỗ trợ giải mã luồng HLS AES-128 và chặn truy cập trái phép 401/403.
* Đưa vào sử dụng bộ trang học tập StudentCoursePlayer và xem trước bài giảng InstructorVideoPreview.
