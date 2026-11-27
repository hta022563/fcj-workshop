---
title: "Chia sẻ, đóng góp ý kiến"
date: 2026-11-20
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### Điều thay đổi lớn nhất sau 3 tháng thực tập

Trước khi vào chương trình **Workforce Bootcamp – First Cloud AI Journey (FCAJ)** tại **Công ty TNHH Amazon Web Services Viet Nam** (14/09/2026 – 14/12/2026), cách làm bài của tôi khá đơn giản: code giao diện React xong, nối API chạy được trên máy mình là coi như ổn. Sau 3 tháng học cùng lớp AWS082025 và làm **Frontend kết hợp kiến trúc** cho dự án **SecureLearn**, góc nhìn của tôi thay đổi khá nhiều.

Làm dự án thật mới thấy chuyện "chạy được" mới chỉ là một nửa, phần còn lại nằm ở bảo mật, chi phí và cách các dịch vụ nối với nhau. Chỉ riêng luồng phát video của SecureLearn thôi cũng kéo theo đủ thứ phải để ý: JWT từ Cognito, Device Fingerprint, đi qua CloudFront và AWS WAF vào backend Spring Boot trên ECS Fargate, tải khóa AES-128 và segment S3 hạn 60 giây, rồi tới lớp Dynamic Watermark 60 FPS với chống PrintScreen ở trình duyệt. May là khi nhóm gửi ảnh sơ đồ kiến trúc qua WhatsApp và nhận được nhận xét góp ý từ sếp Hùng cùng các mentor, nhóm đã kịp sửa từ hướng kết hợp ban đầu sang chạy đồng bộ hoàn toàn trên AWS. Tuy lúc sửa hơi gấp nhưng hệ thống gọn hơn hẳn, lại học thêm được cách tính chi phí thực tế (ví dụ tắt ECS và RDS ngoài giờ làm việc để giảm từ ~$165/tháng xuống còn khoảng ~$60–75/tháng).

### Ấn tượng về môi trường và cộng đồng FCAJ

Ngoài phần tự học theo Coursera, các bài lab trên First Cloud Journey và khóa SAA-C03, tôi thích nhất là những buổi đi sự kiện trực tiếp ở tầng 26 tòa nhà Bitexco. Nghe mấy anh chị kỹ sư từ AWS, CMC Global, STYL Solutions, CloudThinker hay NAB kể về những lỗi thật ngoài doanh nghiệp (như tối ưu chi phí Serverless hay chuyện AI chạy local thì êm nhưng lên production lại vỡ) giúp một sinh viên CNTT từ Đại học FPT như tôi hình dung rõ hơn mình đang thiếu gì và cần học gì tiếp.

Làm chung với các bạn trong nhóm dự án cũng cho tôi nhiều kỷ niệm vui, nhất là mấy lúc cả đám ngồi dò từng lỗi CORS, sửa lại luồng gọi API rồi dọn tài nguyên AWS cuối kỳ. Không khí cởi mở từ mentor tới các bạn cùng lớp khiến việc hỏi bài đỡ ngại hơn nhiều.

### Một vài góp ý nhỏ cho các khóa sau

Từ góc nhìn của người làm Frontend khi nhảy sang dự án Cloud, tôi có ba góp ý nhỏ mong sẽ hữu ích cho các khóa thực tập tiếp theo:

* **Có thêm một bài lab nhỏ về nối Frontend với AWS:** Đa số lab hiện tại thao tác trên Console hoặc CLI. Nếu có thêm phần hướng dẫn ngắn cách nối một trang React/SPA thật với Cognito, bật CloudFront Function cho SPA và upload file lớn qua S3 Presigned URL thì mấy bạn thiên về Frontend sẽ đỡ tốn thời gian mò lỗi tích hợp lúc làm đồ án cuối kỳ.
* **Review kiến trúc sớm tầm tuần 7–8:** Nhóm tôi nhận được rất nhiều góp ý giá trị sau khi gửi sơ đồ kiến trúc qua WhatsApp cho sếp Hùng và các mentor xem, nên nếu có một mốc gửi sơ đồ để góp ý nhanh ngay khi các nhóm mới chốt Proposal thì sẽ tránh được việc code gần xong rồi mới phải sửa lại hạ tầng (như vụ timeout 60 giây của CloudFront hay chi phí ECS/RDS).
* **Thêm vài tình huống tự tìm lỗi (Troubleshooting):** Bên cạnh hướng dẫn làm từng bước suôn sẻ, có thêm một vài bài cố tình gài lỗi nhỏ (thiếu quyền IAM, sai CORS, token hết hạn) sẽ giúp sinh viên quen tay đọc log CloudWatch và tự khoanh vùng lỗi nhanh hơn.

### Lời cảm ơn

Cuối cùng, tôi xin cảm ơn ban tổ chức FCAJ, sếp Hùng, các anh chị mentor, diễn giả và các bạn trong lớp AWS082025 cùng nhóm SecureLearn đã hỗ trợ và đồng hành suốt 3 tháng qua. Kết thúc kỳ thực tập, tôi dự định sẽ tiếp tục ôn để thi chứng chỉ AWS Solutions Architect – Associate (SAA-C03) và rèn thêm cả mảng Frontend lẫn Cloud Architecture cho các dự án tới.
