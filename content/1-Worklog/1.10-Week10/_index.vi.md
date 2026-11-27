---
title: "Tuần 10: Dynamic Watermark 60 FPS, Dashboard Giám sát AI & Truy vết Rò rỉ"
date: 2026-11-16
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Triển khai lớp Dynamic Watermark chuyển động liên tục trên trình phát video để răn đe và truy vết nguồn quay lén màn hình.
* Xây dựng cụm giao diện Quản trị viên: Bảng cảnh báo bất thường AI (AdminAnomalyDashboard), Truy vết rò rỉ (LeakTracing), Quản lý người dùng và Cấu hình hệ thống.
* Phối hợp tích hợp dữ liệu log từ nhánh AI (Isolation Forest + EventBridge + SNS) hiển thị trực quan lên Frontend.
* Hoàn thiện các bài viết Blogs (Blog 1, 2, 3), Proposal và cập nhật báo cáo Events Participated.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Phát triển custom hook useDynamicWatermark dùng requestAnimationFrame (60 FPS) tạo hiệu ứng watermark nảy va chạm biên liên tục (kiểu DVD screensaver). <br> - Hiển thị Student ID cùng timestamp cập nhật từng giây với góc bay và nhiễu vận tốc ngẫu nhiên nhằm chống cắt khung hình khi quay lén. <br> - Nhúng hook vào trình phát bài giảng và kiểm thử hiệu năng render song song với luồng video HLS. | 16/11/2026 | 16/11/2026 | <https://000056.awsfcaj.com/> <br> <https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame> |
| 3 | - Xây dựng AdminAnomalyDashboard kết nối adminService.js lấy danh sách nhật ký truy cập thật (/api/v1/ai/logs) và người dùng Cognito. <br> - Cài đặt hàm buildAnomalyAlertsFromLogs nhóm log theo email để tính toán các tín hiệu bất thường: đa IP, đa thiết bị (fingerprint), spam request key/manifest, lỗi truy cập và tua nhanh. <br> - Bổ sung bộ lọc tìm kiếm, đánh dấu xử lý cảnh báo (resolved) lưu qua localStorage và giao diện xem chi tiết vi phạm. | 17/11/2026 | 17/11/2026 | <https://000200.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 4 | - Thiết kế trang LeakTracing cho phép quản trị viên nhập Watermark ID để truy vết danh tính học viên, khóa học đã cấp quyền, lịch sử phiên và thực hiện khóa tài khoản vi phạm. <br> - Xây dựng trang AdminUserManagement (gọi GET / POST / DELETE /admin/user tích hợp AWS Cognito User Pool qua AdminController). <br> - Hoàn thiện trang AdminSystemConfig tổng hợp dung lượng video, số lượng log, mức chi phí ước tính, ngưỡng điểm AI và chu kỳ xoay vòng khóa KMS. | 18/11/2026 | 18/11/2026 | <https://docs.aws.amazon.com/cognito/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 5 | - Phối hợp đội ngũ hoàn thiện kiến trúc luồng AI Branch Flow (Access Logs → CloudWatch/DynamoDB → EventBridge 5 phút → Lambda Isolation Forest .pkl trên R2 → Amazon SNS). <br> - Rà soát cách thức Frontend tiêu thụ phản hồi và hiển thị thông tin cảnh báo đồng bộ với email SNS của quản trị viên. <br> - Tìm hiểu thêm mẫu bất đồng bộ Amazon SQS và SNS trong các hệ thống giám sát phân tán. | 19/11/2026 | 19/11/2026 | <https://000077.awsfcaj.com/> <br> <https://000083.awsfcaj.com/> |
| 6 | - Cập nhật hoàn chỉnh 3 bài blog kỹ thuật (Blog 1, Blog 2, Blog 3), tài liệu Proposal và danh sách Events Participated lên báo cáo Hugo. <br> - Kiểm thử luồng Admin Portal: tạo/xóa user Cognito, quét log bất thường trên AdminAnomalyDashboard và tra cứu mã watermark trên LeakTracing. <br> - Đối chiếu tiến độ công việc 10 tuần bám sát các giáo trình Coursera, FCJ và SAA-C03. | 20/11/2026 | 20/11/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://cloudjourney.awsfcaj.com/> |

### Kết quả đạt được tuần 10:

* Hoàn thiện Dynamic Watermark 60 FPS (useDynamicWatermark) hỗ trợ truy vết người xem theo thời gian thực ngay trên khung video.
* Đưa vào vận hành trọn bộ Admin Portal gồm AdminAnomalyDashboard, LeakTracing, AdminUserManagement và AdminSystemConfig.
* Hoàn thiện nội dung Blogs 1–3, Events Participated và đồng bộ luồng giám sát AI giữa Frontend và Backend.
