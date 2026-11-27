---
title: "Tuần 5: Cơ sở dữ liệu AWS (RDS, Aurora, DynamoDB & ElastiCache)"
date: 2026-10-12
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Hiểu kiến trúc cơ sở dữ liệu chuyên biệt (Purpose-Built Databases) và sự khác nhau giữa CSDL quan hệ và NoSQL.
* Thực hành triển khai Amazon RDS, tìm hiểu Amazon Aurora (Multi-AZ, Read Replicas, sao lưu tự động).
* Làm chủ Amazon DynamoDB (Partition Key, Sort Key, GSI, Read/Write Capacity Mode, CRUD qua AWS Console và Boto3/CLI) và Amazon ElastiCache.
* Kết nối ứng dụng web với S3 & DynamoDB, hoàn thiện Blog 1 và Blog 3.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu các loại cơ sở dữ liệu chuyên biệt trên AWS: Relational, Key-Value, Document, Graph và In-Memory. <br> - So sánh chi phí vận hành và quản trị giữa CSDL tự cài đặt trên EC2 với Managed Databases. <br> - Khám phá các công cụ truy vấn dữ liệu phi máy chủ như Amazon Athena. | 12/10/2026 | 12/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 3 | - Tìm hiểu kiến trúc Amazon RDS và Amazon Aurora (hiệu năng, khả năng tự động mở rộng storage và Aurora Serverless). <br> - Thực hành khởi tạo RDS DB Instance trong Private Subnet, cấu hình Security Group và kiểm thử kết nối. <br> - Tìm hiểu cơ chế Multi-AZ Failover, Read Replicas và Automated Backups / Snapshots. | 13/10/2026 | 13/10/2026 | <https://000005.awsfcaj.com/> <br> <https://docs.aws.amazon.com/rds/> |
| 4 | - Tìm hiểu khái niệm Partition Key, Sort Key, Global Secondary Index (GSI), Read Consistency và Capacity Mode trên DynamoDB. <br> - Tạo bảng DynamoDB và thực hành thêm, đọc, cập nhật dữ liệu bằng AWS Console. <br> - Sử dụng AWS CloudShell và Python SDK (Boto3) thực hành CRUD, Query, Scan, tạo GSI và cleanup tài nguyên. | 14/10/2026 | 14/10/2026 | <https://000060.awsfcaj.com/> <br> <https://000039.awsfcaj.com/> |
| 5 | - Tìm hiểu Amazon ElastiCache for Redis: tạo Subnet Group, cấu hình Redis Cluster và kiểm thử Set/Get, Hash, Pub/Sub. <br> - Kết nối ứng dụng web mẫu với Amazon S3 và DynamoDB thông qua IAM Role (không dùng khóa tĩnh). <br> - Hoàn thiện bài viết **Blog 3** (*Amazon Linux AMI vs. Windows AMI*). | 15/10/2026 | 15/10/2026 | <https://000061.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 6 | - So sánh tiêu chí chọn loại CSDL phù hợp cho từng mô hình ứng dụng thực tế và hoàn thành bài kiểm tra Module 3. <br> - Hoàn thiện bài viết **Blog 1** (*Quản trị tập trung AWS Account với Organizations & SCPs*). <br> - Thực hiện cleanup RDS Instance, DynamoDB Table và ElastiCache Cluster thử nghiệm. | 16/10/2026 | 16/10/2026 | <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> <br> <https://docs.aws.amazon.com/dynamodb/> |

### Kết quả đạt được tuần 5:

* Nắm vững đặc điểm và tình huống ứng dụng chuẩn xác giữa Amazon RDS/Aurora, Amazon DynamoDB và Amazon ElastiCache.
* Thành thạo thao tác với DynamoDB cả trên AWS Console lẫn CloudShell/Boto3 (CRUD, Query/Scan, thiết kế GSI và Capacity Mode).
* Kết nối thành công ứng dụng web tới tầng dữ liệu qua IAM Role an toàn, hoàn tất Blog 1, Blog 3 và dọn dẹp sạch tài nguyên CSDL.
