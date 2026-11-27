---
title: "Tuần 3: Mạng AWS, Amazon VPC & Route 53"
date: 2026-09-28
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Hiểu các thành phần mạng nền tảng trên AWS: VPC, CIDR, Subnet, Route Table, ENI, Internet Gateway và NAT Gateway.
* Thực hành phân biệt và cấu hình bảo mật hai lớp bằng Security Group (stateful) và Network ACL (stateless).
* Triển khai các mô hình kết nối mạng nâng cao: Session Manager, VPC Endpoint, VPC Peering, Transit Gateway và Route 53 DNS.
* Nắm quy trình khoanh vùng xử lý sự cố mạng và thực hiện cleanup tài nguyên VPC sau thực hành.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu các thành phần cơ bản của AWS Networking: Region, AZ, VPC, Subnet, Route Table, ENI, EIP, Internet Gateway, NAT Gateway, Security Group và NACL. <br> - Thực hành quy hoạch dải IP/CIDR và phân tách Public Subnet với Private Subnet trải trên nhiều AZ. | 28/09/2026 | 28/09/2026 | <https://000003.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| 3 | - Cấu hình bảng định tuyến (Route Tables) kết nối Public Subnet ra Internet Gateway và Private Subnet qua NAT Gateway. <br> - Tìm hiểu dịch vụ phân giải tên miền Route 53 DNS, Internal Hosted Zone, DNS Endpoint và AWS Global Accelerator. <br> - Thực hành cấu hình bản ghi định tuyến cơ bản trên Route 53. | 29/09/2026 | 29/09/2026 | <https://000010.awsfcaj.com/> <br> <https://000092.awsfcaj.com/> |
| 4 | - Tìm hiểu VPC Endpoint (Gateway Endpoint & Interface Endpoint) để truy cập dịch vụ AWS qua mạng riêng. <br> - Thực hành kết nối vào EC2 trong Private Subnet bằng Systems Manager Session Manager mà không cần mở cổng SSH 22. <br> - Tìm hiểu các mô hình liên kết mạng: VPC Peering, Transit Gateway và Site-to-Site VPN. | 30/09/2026 | 30/09/2026 | <https://000058.awsfcaj.com/> <br> <https://000111.awsfcaj.com/> |
| 5 | - Thực hành tạo VPC hoàn chỉnh từ đầu, gắn Subnet, IGW, Route Table và quy tắc Security Group / NACL. <br> - Triển khai thử ứng dụng mẫu vào VPC mới tạo và kiểm tra luồng kết nối giữa tầng Web và tầng dữ liệu. <br> - Kiểm thử chặn/cho phép lưu lượng mạng qua Security Group và NACL. | 01/10/2026 | 01/10/2026 | <https://000020.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 6 | - Thực hành các bước kiểm tra lỗi mạng VPC phổ biến (kiểm tra route 0.0.0.0/0, rule NACL chiều inbound/outbound). <br> - Hoàn thành bài kiểm tra Module 2 trên Coursera và viết bài thu hoạch Event 1 (4.1-Event1). <br> - Thực hiện cleanup VPC, NAT Gateway, Elastic IP và các tài nguyên mạng thử nghiệm. | 02/10/2026 | 02/10/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/vpc-troubleshooting.html> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |

### Kết quả đạt được tuần 3:

* Thiết kế và triển khai thành thạo Amazon VPC đa AZ với đầy đủ Public/Private Subnets, IGW, NAT Gateway và Route Tables.
* Biết cách sử dụng Session Manager và VPC Endpoints nhằm loại bỏ rủi ro phơi bày máy chủ nội bộ ra Internet công cộng.
* Nắm vững cơ chế Route 53, VPC Peering, Transit Gateway và thực hiện cleanup dứt điểm các tài nguyên tính phí như NAT Gateway/EIP.
