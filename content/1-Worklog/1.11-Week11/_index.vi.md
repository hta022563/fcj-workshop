---
title: "Tuần 11: Điều chỉnh Kiến trúc lên AWS, Tinh chỉnh FE & Quay Demo"
date: 2026-11-20
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Sửa lại kiến trúc hệ thống sang thuần AWS theo góp ý của các mentor và sếp Hùng.
* Đưa bản build Frontend React lên Amazon S3 + CloudFront, cấu hình định tuyến SPA và kiểm thử với AWS WAF.
* Kiểm thử lại luồng phát video, bảo mật phía client và nhánh AI v2 trên môi trường AWS mới.
* Quay video demo và cập nhật lại Proposal, Blogs, Workshop cho đồng bộ với nhóm.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Gửi ảnh sơ đồ kiến trúc dự án qua WhatsApp để xin nhận xét từ sếp Hùng và các mentor; dựa trên góp ý đó, cả nhóm thống nhất chuyển toàn bộ hệ thống sang chạy trên AWS (ECS Fargate, ALB, RDS, S3 private, CloudFront, AWS WAF) để dễ quản lý bảo mật và IAM hơn. <br> - Sửa lại file .env.production của FE dùng VITE_API_URL=/api/v1 để gọi API cùng tên miền CloudFront, đỡ rắc rối lỗi CORS. | 23/11/2026 | 23/11/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html> <br> <https://000080.awsfcaj.com/> |
| 3 | - Build React (npm run build) đẩy lên bucket S3 securelearn-web, gắn CloudFront OAC và thêm CloudFront Function securelearn để các route React không bị 404 khi F5. <br> - Chỉnh lại vài lỗi nhỏ về giao diện, kiểm tra Dynamic Watermark khi bật toàn màn hình và đối soát lại trang AdminAnomalyDashboard. | 24/11/2026 | 24/11/2026 | <https://github.com/video-dev/hls.js/> <br> <https://www.framer.com/motion/> |
| 4 | - Phối hợp test luồng upload lên S3 (SSE-KMS), tải segment HLS AES-128 qua presigned URL 60 giây và chạy thử xuất Apple HLS AES-128 trên MediaConvert. <br> - Thử nghiệm các kịch bản chặn bảo mật: gọi API admin ngoài IP allowlist của AWS WAF, gọi thẳng ALB không qua CloudFront (403) và test chống PrintScreen/chuyển tab trên FE. | 25/11/2026 | 25/11/2026 | <https://000098.awsfcaj.com/> <br> <https://000018.awsfcaj.com/> <br> <https://000085.awsfcaj.com/> |
| 5 | - Kiểm thử nhánh AI v2 cùng nhóm: DynamoDB AccessLog Stream (kèm GSI byUserTime) gọi Lambda ECR chạy model isolation_forest_securelearn_v2.pkl, gửi cảnh báo SNS và test khóa user Cognito bằng tài khoản test. <br> - Rà lại bảng dự toán chi phí trên AWS Cost Explorer (~$165/tháng nếu chạy 24/7 hoặc ~$60–75/tháng khi tắt ECS/RDS ngoài giờ). | 26/11/2026 | 26/11/2026 | <https://000074.awsfcaj.com/> <br> <https://000064.awsfcaj.com/> <br> <https://000140.awsfcaj.com/> |
| 6 | - Quay và dựng video demo 5–7 phút chạy toàn bộ luồng trên bản AWS mới. <br> - Đồng bộ lại 3 phần tài liệu nhóm (Proposal, Blogs và Workshop AWS) trên báo cáo Hugo cho khớp với kiến trúc sau khi sửa. | 27/11/2026 | 27/11/2026 | <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://vitejs.dev/guide/build.html> |

### Kết quả đạt được tuần 11:

* Hoàn thành việc chuyển SecureLearn sang kiến trúc thuần AWS theo góp ý của mentor và sếp Hùng, Frontend chạy ổn định trên S3 + CloudFront + WAF.
* Kiểm thử xong các lớp bảo mật từ tầng mạng (WAF, OAC, presigned URL 60 giây) đến tầng trình duyệt (Watermark động, Focus Blackout) và nhánh AI v2.
* Quay xong video demo và cập nhật đồng bộ tài liệu nhóm trên trang báo cáo.
