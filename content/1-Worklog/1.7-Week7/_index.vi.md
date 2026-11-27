---
title: "Tuần 7: Kiến trúc SecureLearn, Thiết kế UI/UX & Khởi tạo Frontend React"
date: 2026-10-26
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Thiết kế kiến trúc tổng thể Hybrid Serverless (AWS + Cloudflare) cho hệ thống SecureLearn, xác định ranh giới Control Plane và Media/Client Plane.
* Nghiên cứu quy chuẩn bảo vệ luồng HLS, quản lý khóa KMS/Secrets Manager và đối chiếu giải pháp theo 6 trụ cột AWS Well-Architected Framework.
* Khởi tạo mã nguồn Frontend ReactJS + Vite + TailwindCSS, xây dựng bộ khung đa ngôn ngữ (i18n) và kiến trúc định tuyến phân quyền theo vai trò.
* Hoàn thiện tài liệu Proposal và tham dự sự kiện AWS First Cloud AI Journey Community Day 2026.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Phân tích bài toán rò rỉ video bài giảng tại các trung tâm giáo dục SMEs và nhược điểm chi phí của DRM thương mại. <br> - Chốt phạm vi In-Scope (HLS/AES-128, JWT, short-lived playback token, Device Fingerprint, Dynamic Watermark, AI log anomaly) và Out-of-Scope. <br> - Tham gia định hình kiến trúc Event-Driven phối hợp giữa Frontend React, API Gateway/Lambda và Cloudflare R2. | 26/10/2026 | 26/10/2026 | <https://000054.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 3 | - Tìm hiểu luồng hoạt động của AWS Elemental MediaConvert, Cloudflare R2 (tương thích S3 API, Zero Egress Fee) và chuẩn mã hóa HLS AES-128. <br> - Nghiên cứu cơ chế bảo mật khóa bằng AWS KMS (CMK), Secrets Manager và nguyên tắc phân tách trách nhiệm Control Plane – Media Plane. <br> - Thống nhất hợp đồng API (API contract) giữa đội Frontend và Backend cho các luồng xác thực, upload và phát video. | 27/10/2026 | 27/10/2026 | <https://000033.awsfcaj.com/> <br> <https://000096.awsfcaj.com/> |
| 4 | - Thiết kế và hoàn thiện 3 sơ đồ kiến trúc luồng dữ liệu: Upload Flow, Playback Flow và AI Branch Flow. <br> - Đánh giá bản thiết kế SecureLearn qua 6 trụ cột Well-Architected (Security, Reliability, Operational Excellence, Performance, Cost, Sustainability). <br> - Lập bảng dự toán chi phí vận hành (~$46–$48.60 USD/tháng) và ma trận đánh giá rủi ro cho dự án. | 28/10/2026 | 28/10/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| 5 | - Khởi tạo dự án Frontend React 18 + Vite 5.4 + TailwindCSS 3.4 + Framer Motion + Lucide Icons trong thư mục client. <br> - Xây dựng tầng nền tảng giao diện: ThemeContext (Dark/Light Mode), ToastProvider, MeshGradientBackground, ParticleBackground và ErrorBoundary. <br> - Tích hợp đa ngôn ngữ Việt – Anh bằng i18next / react-i18next với LayoutWithLanguage và LanguageSwitcher. | 29/10/2026 | 29/10/2026 | <https://react.dev/> <br> <https://tailwindcss.com/docs> |
| 6 | - Thiết kế kiến trúc routing trong App.jsx kết hợp ProtectedRoute phân tách 3 cổng làm việc: Student, Instructor và Administrator theo vai trò từ JWT. <br> - Xây dựng khung điều hướng RolePortalLayout, MainNavbar và hoàn thiện tài liệu Proposal song ngữ. <br> - Tham dự AWS First Cloud AI Journey Community Day 2026 (31/10/2026) tại Bitexco Financial Tower. | 30/10/2026 | 31/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://reactrouter.com/> |

### Kết quả đạt được tuần 7:

* Hoàn thiện tài liệu kiến trúc tổng thể SecureLearn theo chuẩn AWS Well-Architected cùng 3 sơ đồ luồng dữ liệu và bảng hợp đồng API giữa FE – BE.
* Dựng xong khung ứng dụng Frontend ReactJS + TailwindCSS hỗ trợ Dark Mode, song ngữ Việt – Anh (i18next) và phân nhánh Portal theo vai trò.
* Hoàn tất Proposal dự án và cập nhật kiến thức thực tế về Cloud Architecture tại sự kiện Community Day.
