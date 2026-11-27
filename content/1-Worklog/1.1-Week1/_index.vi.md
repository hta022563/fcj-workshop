---
title: "Tuần 1: Tổng quan AWS, Bảo mật IAM & Quản lý chi phí"
date: 2026-09-14
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Làm quen môi trường thực tập First Cloud AI Journey, hạ tầng toàn cầu của AWS và các phương thức thao tác qua Console, CLI và API.
* Nắm vững Mô hình Trách nhiệm Chung (Shared Responsibility Model) và các bước bảo vệ tài khoản Root User.
* Thực hành quản trị định danh với AWS IAM (User, Group, Role, Policy, Permission Boundary) theo nguyên tắc đặc quyền tối thiểu.
* Cấu hình ngân sách AWS Budgets, thiết lập cảnh báo chi phí và dọn dẹp tài nguyên sau thực hành.

### Các công việc triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Làm quen với chương trình First Cloud AI Journey và quy định làm việc tại đơn vị thực tập. <br> - Tìm hiểu tổng quan điện toán đám mây, khái niệm Region, Availability Zone và Edge Location. <br> - Tạo tài khoản AWS Free Tier, cài đặt AWS CLI và kiểm tra cấu hình xác thực ban đầu. | 14/09/2026 | 14/09/2026 | <https://000001.awsfcaj.com/> <br> <https://000011.awsfcaj.com/> |
| 3 | - Tìm hiểu ranh giới bảo mật trong Shared Responsibility Model và cách hoạt động của AWS API. <br> - Phân biệt Root User với IAM User và bật xác thực đa yếu tố (MFA) cho tài khoản gốc. <br> - Tạo Access Key phục vụ AWS CLI và áp dụng quy tắc không dùng Root User hằng ngày. | 15/09/2026 | 15/09/2026 | <https://000002.awsfcaj.com/> <br> <https://000009.awsfcaj.com/> |
| 4 | - Tìm hiểu 4 thành phần cốt lõi của IAM: User, Group, Role và JSON Policy. <br> - Tạo các nhóm Admin, IT, Management, gán IAM User và viết Policy theo Least Privilege. <br> - Khám phá Permission Boundary, SCPs và kiểm thử quyền truy cập bằng IAM Policy Simulator. | 16/09/2026 | 16/09/2026 | <https://000030.awsfcaj.com/> <br> <https://000044.awsfcaj.com/> |
| 5 | - Thực hành tạo IAM Role và chuyển đổi quyền tạm thời (Switch Role) với thời lượng Session giới hạn. <br> - Thiết lập Cost Budget, Usage Budget, RI Budget và Savings Plans Budget trên AWS Billing. <br> - Cấu hình ngưỡng cảnh báo chi phí tại 12.5%, 50%, 80% gửi về nhiều email quản trị. | 17/09/2026 | 17/09/2026 | <https://000007.awsfcaj.com/> <br> <https://coursera.org/share/350b9ff51be9a40049a2b813ee6f775d> |
| 6 | - Kiểm tra chéo quyền thực thi của từng User, Group và Role sau khi phân quyền. <br> - Hoàn thành bài kiểm tra tổng hợp kiến thức nền tảng bảo mật & IAM trên Coursera. <br> - Thực hiện dọn dẹp User, Group, Role, Policy, Budget và Access Key thử nghiệm. | 18/09/2026 | 18/09/2026 | <https://www.youtube.com/watch?v=c3Cn4xYfxJY> <br> <https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html> |

### Kết quả đạt được tuần 1:

* Khởi tạo thành công tài khoản AWS Free Tier, kích hoạt MFA bảo vệ Root User và sử dụng song song AWS Console cùng AWS CLI.
* Nắm vững cấu trúc IAM Policy dạng JSON, biết cách giới hạn quyền bằng Permission Boundary và kiểm tra trước khi áp dụng thực tế.
* Thiết lập hoàn chỉnh hệ thống cảnh báo chi phí AWS Budgets đa ngưỡng và nắm quy trình cleanup tài nguyên sạch sẽ sau mỗi bài lab.
