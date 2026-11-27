---
title: "Tuần 8: Frontend Xác thực Cognito, Device Fingerprint & Luồng Upload Video"
date: 2026-11-02
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Xây dựng hoàn chỉnh các giao diện công khai (Trang chủ, Danh mục khóa học, Chi tiết bài giảng) và cổng đăng nhập/đăng ký tích hợp Cognito JWT.
* Triển khai dịch vụ tạo định danh thiết bị (Device Fingerprint) phía trình duyệt phục vụ kiểm soát phiên và chống chia sẻ tài khoản.
* Hiện thực hóa luồng tải video bài giảng lên Cloudflare R2 trực tiếp từ trình duyệt giảng viên (Presigned URL Upload Pipeline).
* Phối hợp kiểm thử kết nối giữa React Frontend với API Backend (Spring Boot & AWS API Gateway).

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng các trang giao diện Home (kèm HeroStatsCard, LearningTimeline), CourseCatalog, SubjectLectures và MyCourses. <br> - Lập trình courseService.js, subjectService.js và entitlementService.js giao tiếp API danh mục khóa học và quyền ghi danh. <br> - Tạo các modal nghiệp vụ CreateCourseModal và CreateSubjectModal cho giao diện quản lý nội dung. | 02/11/2026 | 02/11/2026 | <https://000078.awsfcaj.com/> <br> <https://react.dev/> |
| 3 | - Phát triển cụm xác thực phía Frontend: Login, Register, OtpInput (xác thực OTP Cognito) và ForgotPasswordModal. <br> - Hoàn thiện AuthContext quản lý trạng thái đăng nhập bằng sessionStorage, đồng bộ authService.js (register, login, refresh, logout toàn cầu). <br> - Cấu hình Axios Interceptor trong axiosClient.js tự động đính kèm Bearer JWT cho mọi yêu cầu tới Backend. | 03/11/2026 | 03/11/2026 | <https://000081.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 4 | - Tích hợp thư viện FingerprintJS (@fingerprintjs/fingerprintjs) vào fingerprintService.js để trích xuất visitorId thực tế của trình duyệt và thiết bị. <br> - Cài đặt cơ chế fallback băm SHA-256 qua Web Crypto API từ userAgent, ngôn ngữ, độ phân giải màn hình và múi giờ khi FingerprintJS bị chặn. <br> - Lưu đệm device_fingerprint trong sessionStorage và tự động gắn header X-Device-Fingerprint trên các luồng auth và playback. | 04/11/2026 | 04/11/2026 | <https://github.com/fingerprintjs/fingerprintjs> <br> <https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto> |
| 5 | - Thiết kế giao diện giảng viên gồm InstructorVideos, UploadVideo và ReuploadVideoModal phục vụ đăng tải và cập nhật bài giảng. <br> - Xây dựng custom hook useVideoUpload cùng uploadService.js thực thi quy trình 3 bước: xin Presigned URL, PUT file thẳng lên Cloudflare R2 và gọi /upload/process chuyển mã HLS. <br> - Hiển thị thanh tiến trình theo byte thực tế (uploading, processing, ready, error) và chặn memory leak khi component unmount bằng useRef. | 05/11/2026 | 05/11/2026 | <https://000137.awsfcaj.com/> <br> <https://developers.cloudflare.com/r2/> |
| 6 | - Phối hợp với Backend kiểm thử toàn bộ Upload Flow: Giảng viên chọn file trên UploadVideo → R2 Presigned Upload → Transcode HLS → Cập nhật danh mục bài giảng. <br> - Kiểm tra xử lý lỗi mạng, hủy tải giữa chừng và phân quyền truy cập trang Instructor với ProtectedRoute. <br> - Rà soát tài liệu API tích hợp giữa Frontend và tầng lưu trữ Cloudflare R2. | 06/11/2026 | 06/11/2026 | <https://000066.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Kết quả đạt được tuần 8:

* Hoàn thiện giao diện Home, Catalog, cụm đăng nhập/đăng ký OTP Cognito và cơ chế AuthContext + Axios JWT Interceptor.
* Triển khai thành công fingerprintService.js sinh device_fingerprint thực tế gửi kèm header X-Device-Fingerprint.
* Đưa vào chạy ổn định luồng upload video trực tiếp lên Cloudflare R2 từ Frontend giảng viên (UploadVideo + useVideoUpload).
