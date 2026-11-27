---
title: "Tuần 2: Dịch vụ Compute trên AWS (EC2, Containers & Serverless)"
date: 2026-09-21
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Nắm vững các mô hình điện toán trên AWS từ máy ảo (EC2), container (ECS/EKS/Fargate) đến serverless (AWS Lambda).
* Thực hành khởi tạo, quản lý vòng đời EC2 Instance, kết nối SSH, gắn EBS volume và sử dụng IAM Instance Profile.
* Phân tích sự khác biệt giữa Amazon Linux 2023 và Windows Server AMI về tài nguyên và chi phí bản quyền.
* Tham dự sự kiện khởi động Buildrathon Kickoff để tiếp cận xu hướng Generative AI và AI Agent.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu mô hình Compute as a Service, các họ EC2 Instance và cách chọn cấu hình vCPU/RAM phù hợp. <br> - So sánh các hình thức tính phí EC2: On-Demand, Reserved Instances, Spot Instances và Savings Plans. <br> - Tìm hiểu vai trò của Amazon Machine Image (AMI) khi đóng gói hệ điều hành và phần mềm. | 21/09/2026 | 21/09/2026 | <https://000004.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| 3 | - Tìm hiểu vòng đời trạng thái của EC2 Instance (Pending, Running, Stopping, Stopped, Terminated) và Elastic IP. <br> - Khởi tạo máy chủ EC2 dùng Amazon Linux 2023 AMI, tạo Key Pair và kết nối SSH từ máy cá nhân. <br> - Gắn thêm EBS volume và cấu hình IAM Instance Profile cho EC2 thay cho việc lưu Access Key tĩnh. | 22/09/2026 | 22/09/2026 | <https://000048.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 4 | - Tìm hiểu kiến trúc đóng gói Docker và các dịch vụ điều phối container gồm Amazon ECR, Amazon ECS và Amazon EKS. <br> - Thực hành triển khai container không cần quản trị máy chủ với AWS Fargate. <br> - So sánh chi phí vận hành và độ linh hoạt giữa EC2 truyền thống và container trên Fargate. | 23/09/2026 | 23/09/2026 | <https://000015.awsfcaj.com/> <br> <https://000067.awsfcaj.com/> |
| 5 | - Tìm hiểu kiến trúc hướng sự kiện (event-driven) của AWS Lambda, Execution Role và giới hạn thực thi. <br> - Viết hàm Lambda xử lý đầu vào JSON mẫu, kiểm tra log thực thi và phân tích cơ chế tính phí theo request. <br> - Đối chiếu chi tiết Amazon Linux 2023 và Windows Server AMI để tổng hợp bài viết Blog 3. | 24/09/2026 | 24/09/2026 | <https://000022.awsfcaj.com/> <br> <https://docs.aws.amazon.com/linux/al2023/ug/what-is-amazon-linux.html> |
| 6 | - Tham khảo phương pháp tối ưu kích thước máy chủ Right-Sizing cho EC2 và kiểm tra tài nguyên đang chạy. <br> - Thực hiện terminate các EC2 instance, xóa volume/snapshot thừa và dọn dẹp tài nguyên lab. <br> - Chuẩn bị nội dung và tham dự sự kiện Buildrathon Kickoff cùng CMC Global (26/09/2026). | 25/09/2026 | 25/09/2026 | <https://000032.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |

### Kết quả đạt được tuần 2:

* Thành thạo quy trình khởi tạo EC2, kết nối SSH, gắn EBS volume và cấp quyền an toàn cho máy chủ qua IAM Instance Profile.
* Hiểu rõ khi nào nên chọn EC2, ECS/EKS với Fargate hay AWS Lambda dựa trên đặc tính tải và ngân sách.
* Hoàn tất phân tích đánh đổi giữa Linux AMI và Windows AMI (tài nguyên RAM, SSH vs. RDP, phí bản quyền OS) và dọn dẹp sạch tài nguyên sau thực hành.
