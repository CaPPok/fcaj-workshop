---
title: "Worklog Tuần 2"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

- Khám phá hệ sinh thái AI/ML trên AWS và đi sâu vào dịch vụ Amazon SageMaker.
- Nắm vững các khái niệm và cách thiết lập luồng vận hành Machine Learning - MLOps trên môi trường Cloud.
- Khám phá nhóm dịch vụ Data & Analytics trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Khám phá tổng quan AI/ML services trên AWS. <br> - Hiểu sự khác biệt giữa các dịch vụ AI xây dựng sẵn và việc tự phát triển mô hình. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Nghiên cứu về Amazon SageMaker. <br> - Tìm hiểu các thành phần cốt lõi: SageMaker Studio, Processing Jobs và SageMaker Endpoints. | 16/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Thực hành sử dụng Amazon SageMaker Studio | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Tìm hiểu về kiến trúc và cấu hình vòng đời MLOps. <br> - Phân tích cách tự động hóa quy trình: thu thập dữ liệu -> huấn luyện -> đánh giá -> triển khai. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Học chuyên đề Data & Analytics trên AWS. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/vi/6-dataandanalytic/> |

### Kết quả đạt được tuần 2:

* **Biết cơ bản về hệ sinh thái AI/ML:** Hiểu cách AWS phân chia các tầng dịch vụ AI/ML. Nắm được vai trò trung tâm của Amazon SageMaker trong việc phát triển các mô hình tùy chỉnh thay vì chỉ dùng các API có sẵn.
* **Hiểu về SageMaker:** Phân biệt rõ ràng giữa hai luồng tác vụ quan trọng sẽ dùng trong dự án:
  * **Processing Job:** Dành cho việc chạy ngầm quy trình retrain định kỳ.
  * **Real-time Endpoint:** Dành cho việc tải mô hình 24/7 để phục vụ dự đoán tức thì cho Backend.
* **Tư duy thiết kế MLOps:** Hiểu được sự cần thiết của việc xây dựng một luồng CI/CD cho Machine Learning, bao gồm việc đặt ra các rào cản chất lượng trước khi đưa mô hình mới lên thay thế mô hình cũ.
* **Mở rộng về Data & Analytics:** 
  * Nắm bắt được các phương pháp thu thập, xử lý và lưu trữ dữ liệu quy mô lớn.
  * Hiểu được vai trò của Data Lake so với Data Warehouse truyền thống,.