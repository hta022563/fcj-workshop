---
title: "Tự đánh giá"
date: 2026-11-20
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Kết thúc kỳ thực tập **Workforce Bootcamp – First Cloud AI Journey (FCAJ)** tại **Công ty TNHH Amazon Web Services Viet Nam** (14/09/2026 – 14/12/2026), điều tôi cảm thấy rõ nhất không phải là mình đã giỏi cloud ngay lập tức, mà là bản thân đã bớt sợ và biết cách làm việc bài bản hơn rất nhiều.

Mấy tuần đầu mới mở AWS Console, thú thật tôi khá khớp vì giao diện có quá nhiều dịch vụ, cứ sợ bấm nhầm cái gì đó rồi cuối tháng bị trừ tiền. Nhờ vậy mà tôi tập được thói quen làm việc cẩn thận ngay từ đầu: bật MFA cho tài khoản gốc, không dùng Root User linh tinh và tạo sẵn AWS Budgets cảnh báo từ mốc 12.5% rồi mới dám tạo VPC hay EC2. Mấy buổi đi nghe chia sẻ trực tiếp ở tòa nhà Bitexco cũng giúp tôi đỡ bỡ ngỡ, thấy được cách mấy anh chị đi trước dùng Cloud ngoài thực tế khác với lúc học lý thuyết trên trường ra sao.

Đến giai đoạn làm dự án **SecureLearn** từ tuần 7, tôi đảm nhận mảng **Frontend và góp phần thiết kế kiến trúc**. Lúc làm mới thấy nhiều thứ không đơn giản như tưởng tượng: có mấy tối ngồi gỡ lỗi trình phát HLS.js mãi không tải được khóa AES-128, rồi chỉnh đi chỉnh lại lớp Dynamic Watermark 60 FPS sao cho bật toàn màn hình không bị lệch. Nhất là gần cuối kỳ, khi nhóm gửi ảnh sơ đồ kiến trúc qua WhatsApp và nhận được góp ý từ sếp Hùng cùng các mentor, cả nhóm quyết định sửa lại kiến trúc sang chạy hẳn trên AWS (S3, CloudFront, WAF, ECS Fargate, RDS) nên cũng khá gấp để chỉnh lại cấu hình FE và test lại từ đầu. Dù hơi mệt nhưng lúc thấy bấm PrintScreen màn hình tự phủ đen, log truy cập thật đổ về AdminAnomalyDashboard và truy vết được mã watermark trên LeakTracing, cảm giác rất đã.

Tất nhiên làm xong nhìn lại tôi cũng thấy mình còn nhiều chỗ chưa tốt. Dưới đây là phần tôi tự chấm thẳng thắn cho bản thân sau 3 tháng:

| STT | Tiêu chí | Mô tả | Tốt | Khá | Trung bình |
| --- | --- | --- | --- | --- | --- |
| 1 | **Kiến thức và kỹ năng chuyên môn** | Hiểu biết về Cloud/Frontend, áp dụng vào SecureLearn, chất lượng đầu ra | ☐ | ✅ | ☐ |
| 2 | **Khả năng học hỏi** | Tiếp thu công nghệ mới (AWS, HLS.js, cách triển khai SPA lên CloudFront) | ✅ | ☐ | ☐ |
| 3 | **Chủ động** | Tự đọc tài liệu, chủ động nhận việc FE & trao đổi kiến trúc với nhóm | ✅ | ☐ | ☐ |
| 4 | **Tinh thần trách nhiệm** | Bám sát phần việc của mình, cố gắng hoàn thành kịp các mốc demo | ✅ | ☐ | ☐ |
| 5 | **Quản lý thời gian & Kỷ luật** | Cân đối thời gian giữa code, test và viết báo cáo | ☐ | ☐ | ✅ |
| 6 | **Tính cầu tiến** | Tiếp thu góp ý từ mentor, sếp Hùng và đồng đội để sửa lại hệ thống | ✅ | ☐ | ☐ |
| 7 | **Giao tiếp & Thuyết trình** | Trình bày ý tưởng kỹ thuật, đặt câu hỏi và nói trước nhiều người | ☐ | ☐ | ✅ |
| 8 | **Hợp tác nhóm** | Phối hợp giữa Frontend React với đội Backend/Cloud khi tích hợp API | ✅ | ☐ | ☐ |
| 9 | **Ứng xử chuyên nghiệp** | Tôn trọng đồng đội, mentor và giữ tác phong nghiêm túc | ✅ | ☐ | ☐ |
| 10 | **Tư duy giải quyết vấn đề** | Tự lần tìm nguyên nhân lỗi CORS, phát video HLS và luồng phân quyền | ☐ | ✅ | ☐ |
| 11 | **Đóng góp vào dự án/nhóm** | Hoàn thiện 3 cổng giao diện FE, lớp chống quay lén và đồng thiết kế luồng dữ liệu | ☐ | ✅ | ☐ |
| 12 | **Tổng thể** | Đánh giá chung cho cả kỳ thực tập | ☐ | ✅ | ☐ |

### Những điểm tôi thấy mình làm được

* **Không còn chỉ nhìn góc độ giao diện:** Trước đây tôi chỉ quen code React chạy cục bộ, giờ đã hiểu rõ đường đi của request qua CloudFront, WAF, ALB vào Backend, hiểu vì sao cần CloudFront Function cho SPA hay vì sao cần gửi kèm JWT và Device Fingerprint.
* **Tự tay làm được phần bảo mật phía Client:** Bộ hook bảo vệ video (useSecureHls, useSecurePlayer, useDynamicWatermark, useVideoVisibility) giúp trình phát hoạt động ổn định và phục vụ đúng bài toán chống tải lậu của dự án.
* **Kiên trì cùng nhóm đến lúc chạy thật:** Kể cả lúc phải đổi kiến trúc sang thuần AWS sát tuần cuối, cả nhóm vẫn phối hợp sửa kịp cấu hình, test lại đủ luồng và quay xong demo.

### Những chỗ còn yếu cần tự sửa

* **Giao tiếp & trình bày (Trung bình):** Tôi vẫn hay bị run khi đứng giải thích kiến trúc trước mentor, nhiều khi hiểu trong đầu nhưng nói ra lại dài dòng, chưa đi thẳng vào ý chính. Sau đợt này tôi cần tập tóm tắt vấn đề ngắn gọn hơn và hỏi sớm hơn thay vì tự mày mò quá lâu.
* **Quản lý thời gian (Trung bình):** Có mấy hôm tôi bị cuốn vào việc chỉnh hiệu ứng hay sửa tiểu tiết giao diện trên React nên lúc gần deadline viết báo cáo và test hơi bị cập rập. Tôi cần tập ưu tiên chạy được luồng chính trước rồi mới trau chuốt UI sau.
* **Kỹ năng vận hành Backend/DevOps (Khá):** Tôi đọc hiểu được luồng triển khai ECS, RDS, Lambda trên AWS nhưng kinh nghiệm tự tay dựng và tối ưu hạ tầng production từ đầu vẫn còn mỏng. Thời gian tới tôi sẽ tiếp tục luyện thêm qua các lab thực tế và ôn thi chứng chỉ AWS Solutions Architect – Associate (SAA-C03).
