---
title: "Tuần 6: Giám sát CloudWatch, High Availability & Tối ưu hóa"
date: 2026-10-19
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Thực hành thu thập Metrics, Logs, thiết lập Alarms trên Amazon CloudWatch và kiểm toán hành động qua AWS CloudTrail.
* Triển khai kiến trúc tính sẵn sàng cao (High Availability) đa AZ kết hợp Elastic Load Balancing và EC2 Auto Scaling.
* Nắm vững 6 trụ cột của AWS Well-Architected Framework và các chiến lược tối ưu hóa chi phí đám mây.
* Hoàn thành bài đánh giá cuối khóa AWS Cloud Technical Essentials và dọn dẹp tài nguyên lab.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu cơ chế thu thập Metrics, Log Groups, Dashboards và đặt ngưỡng cảnh báo Alarms trên Amazon CloudWatch. <br> - Khám phá AWS CloudTrail ghi nhận lịch sử gọi API và tích hợp trực quan hóa log với CloudWatch / Grafana. <br> - Cấu hình cảnh báo CPU Utilization gửi thông báo tự động qua email. | 19/10/2026 | 19/10/2026 | <https://000008.awsfcaj.com/> <br> <https://000029.awsfcaj.com/> |
| 3 | - Tìm hiểu kiến trúc Application Load Balancer (ALB), Network Load Balancer (NLB), Target Group và Health Check. <br> - Tạo Launch Template và cấu hình EC2 Auto Scaling Group tự động tăng giảm số lượng máy chủ theo tải CPU. <br> - Kiểm thử phân phối tải đều qua nhiều Availability Zones. | 20/10/2026 | 20/10/2026 | <https://000006.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 4 | - Thực hành triển khai ứng dụng web có tính sẵn sàng cao (High Availability) kết hợp ALB + Auto Scaling đa AZ. <br> - Mô phỏng tắt đột ngột một EC2 instance để kiểm chứng khả năng tự phát hiện lỗi và khởi tạo máy chủ thay thế. <br> - Kiểm tra tính liên tục của dịch vụ không bị gián đoạn khi một AZ gặp sự cố. | 21/10/2026 | 21/10/2026 | <https://000101.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| 5 | - Nghiên cứu 6 trụ cột AWS Well-Architected: Security, Reliability, Operational Excellence, Performance, Cost & Sustainability. <br> - Tìm hiểu công cụ AWS Compute Optimizer, Savings Plans, Reserved Instances và cách trực quan hóa chi phí. <br> - Phân tích các mẫu tối ưu hóa tài nguyên cho hệ thống vừa và nhỏ. | 22/10/2026 | 22/10/2026 | <https://000042.awsfcaj.com/> <br> <https://000034.awsfcaj.com/> |
| 6 | - Hệ thống lại toàn bộ kiến thức 4 phần: IAM/Security, Compute/Networking, Storage/DB và Monitoring/HA. <br> - Hoàn thành bài kiểm tra cuối khóa **End of Course Assessment** nhận chứng chỉ AWS Cloud Technical Essentials. <br> - Thực hiện cleanup ALB, Target Group, Auto Scaling Group, Launch Template và CloudWatch Alarms. | 23/10/2026 | 23/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://000036.awsfcaj.com/> |

### Kết quả đạt được tuần 6:

* Thiết lập thành thạo hệ thống giám sát CloudWatch Metrics/Alarms, CloudTrail audit và kiến trúc High Availability đa AZ với ALB + Auto Scaling.
* Đạt chứng chỉ hoàn thành khóa học **AWS Cloud Technical Essentials** trên Coursera và nắm vững 6 trụ cột AWS Well-Architected.
* Thực hiện cleanup toàn bộ hạ tầng HA thử nghiệm, sẵn sàng chuyển sang giai đoạn thiết kế và xây dựng dự án **SecureLearn**.
