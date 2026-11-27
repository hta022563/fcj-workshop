---
title: "Tuần 4: Lưu trữ AWS (EBS, EFS, S3 & CloudFront)"
date: 2026-10-05
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Phân biệt rõ Block Storage (Instance Store, Amazon EBS), File Storage (Amazon EFS, FSx) và Object Storage (Amazon S3).
* Thực hành tạo và bảo mật Amazon S3 Bucket (Block Public Access, Bucket Policy, Encryption, Presigned URL, Lifecycle Rules).
* Triển khai tự động hóa EBS Snapshot, sao lưu với AWS Backup và phân phối nội dung toàn cầu qua Amazon CloudFront.
* Hoàn thiện bài viết Blog 2 về Zero Trust & Least Privilege và dọn dẹp tài nguyên thực hành.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu 3 nhóm dịch vụ lưu trữ trên AWS: Block, File và Object Storage cùng tiêu chí chọn theo IOPS và độ trễ. <br> - Khám phá cấu trúc Bucket, Object Key, độ bền 11 số 9 (99.999999999%) và các Storage Classes trên Amazon S3. <br> - Tìm hiểu quy tắc tự động chuyển tầng lưu trữ (Lifecycle Policies) và Replication. | 05/10/2026 | 05/10/2026 | <https://000068.awsfcaj.com/> <br> <https://www.youtube.com/watch?v=c3Cn4xYfxJY> |
| 3 | - Phân biệt lưu trữ tạm thời EC2 Instance Store với Amazon EBS (gp3, io2) và hệ thống file chia sẻ đa AZ Amazon EFS / FSx. <br> - Thực hành tự động hóa chụp và xóa bản sao lưu theo lịch bằng EBS Data Lifecycle Manager. <br> - Tìm hiểu giải pháp sao lưu tập trung AWS Backup. | 06/10/2026 | 06/10/2026 | <https://000088.awsfcaj.com/> <br> <https://000013.awsfcaj.com/> |
| 4 | - Tạo S3 Bucket trên AWS Console, bật Versioning và cấu hình Static Website Hosting thử nghiệm. <br> - Thực hành các thao tác upload, đồng bộ thư mục (aws s3 cp, aws s3 sync) qua AWS CLI và CloudShell. <br> - Kiểm thử khôi phục phiên bản tệp cũ khi xóa nhầm đối tượng có bật Versioning. | 07/10/2026 | 07/10/2026 | <https://000057.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| 5 | - Thực hành cấu hình bảo mật S3: bật Block Public Access, viết Bucket Policy, thiết lập mã hóa SSE-S3 / SSE-KMS. <br> - Tìm hiểu cơ chế tạo Presigned URL giới hạn thời gian truy cập tệp riêng tư. <br> - Tạo CloudFront Distribution trỏ về S3 với Origin Access Control (OAC) để phân phối nội dung bảo mật tại biên. | 08/10/2026 | 08/10/2026 | <https://000069.awsfcaj.com/> <br> <https://000094.awsfcaj.com/> |
| 6 | - Đối chiếu các bài toán chọn dịch vụ lưu trữ tối ưu chi phí theo tần suất truy cập dữ liệu. <br> - Tổng hợp và hoàn thiện bài viết **Blog 2** (*AWS Security: Zero Trust & Least Privilege*). <br> - Thực hiện cleanup toàn bộ S3 Bucket, CloudFront Distribution và EBS Snapshot thử nghiệm. | 09/10/2026 | 09/10/2026 | <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://docs.aws.amazon.com/s3/> |

### Kết quả đạt được tuần 4:

* Nắm vững đặc tính kỹ thuật và bài toán áp dụng của Instance Store, Amazon EBS, Amazon EFS, Amazon S3 và CloudFront.
* Thực hành thành thạo bảo mật S3 Bucket, tạo Presigned URL và tích hợp CloudFront OAC tránh lộ bucket ra công khai.
* Hiểu cách thiết lập Lifecycle Rules và tự động hóa snapshot để kiểm soát chi phí lưu trữ lâu dài, hoàn thiện Blog 2 và cleanup sạch tài nguyên.
