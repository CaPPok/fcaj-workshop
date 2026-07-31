---
title: "Worklog Tuần 1"
date: 2026-07-30
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

- Làm quen với môi trường làm việc, quy trình và các thành viên trong dự án First Cloud AI Journey.
- Nắm rõ quy định và nội quy văn phòng.
- Thiết lập thành công tài khoản AWS cá nhân và làm chủ các công cụ giao tiếp với AWS.
- Nắm vững kiến trúc và cách vận hành của các dịch vụ Cloud cốt lõi.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Làm quen team FCAJ, đọc nội quy văn phòng. <br> - Tạo tài khoản AWS Free Tier. <br> - Cài đặt, cấu hình và làm quen với thao tác trên AWS Management Console & AWS CLI. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tìm hiểu AWS IAM (Identity and Access Management): User, Group, Role, Policy. <br> - Tìm hiểu Amazon S3: Bucket, Object, các khái niệm lưu trữ cơ bản. <br> - **Thực hành:** Khởi tạo user/policy trên IAM và tạo S3 Bucket đầu tiên. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Tìm hiểu Amazon EC2: Instance types, AMI, cơ chế bảo mật (Security Groups), EBS. <br> - **Thực hành:** Tạo EC2 instance, thiết lập Key Pair và kết nối thành công qua SSH. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Nghiên cứu Amazon DynamoDB. <br> - Tìm hiểu cơ chế Partition Key, Sort Key, và Schema-less design để chuẩn bị cho việc lưu trữ metadata phim. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Tìm hiểu về Amazon Athena. <br> - Viết Blog Post tổng kết kiến thức tuần 1, chia sẻ về cách truy vấn dữ liệu serverless không cần dựng Database truyền thống. | 12/06/2026 | 12/06/2026 | <https://docs.aws.amazon.com/athena/latest/ug/what-is.html> |

### Kết quả đạt được tuần 1:

* **Hòa nhập môi trường:** Đã nắm rõ quy trình làm việc, nội quy văn phòng và kết nối tốt với các thành viên trong dự án First Cloud AI Journey.
* **Làm chủ công cụ:** Thiết lập thành công môi trường AWS CLI trên máy cá nhân (cấu hình Access Key, Secret Key, Region) và sử dụng thành thạo AWS Management Console.
* **Kiến thức hạ tầng cốt lõi:**
  * Hiểu và vận dụng cơ chế phân quyền bảo mật (IAM) theo nguyên tắc đặc quyền tối thiểu.
  * Khởi tạo và kết nối SSH thành công máy chủ ảo EC2.
  * Hiểu cơ chế lưu trữ hướng đối tượng của Amazon S3 và cơ sở dữ liệu NoSQL với Amazon DynamoDB.
* **Mở rộng tư duy với Amazon Athena:** 
  * Nắm được bản chất của Amazon Athena: Là một dịch vụ serverless mạnh mẽ cho phép truy vấn trực tiếp dữ liệu lưu trên S3 bằng cú pháp SQL chuẩn.
  * Nhận thấy ưu điểm tuyệt đối trong việc giảm tải quản lý hạ tầng: Không cần tạo máy chủ, tương thích tốt với nhiều định dạng dữ liệu, rất hữu ích cho quá trình phân tích dữ liệu huấn luyện mô hình Machine Learning.