---
title: "Worklog Tuần 7"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

- Ôn tập và nắm vững cách vận hành các dịch vụ cốt lõi gồm Amazon SageMaker, Amazon S3, SageMaker Processing Jobs và SageMaker Endpoints.
- Triển khai mô hình lên môi trường đám mây phục vụ việc huấn luyện, tái huấn luyện và lưu trữ artifact.
- Tích hợp mô hình gợi ý với hệ thống giao diện và máy chủ backend do các thành viên khác trong nhóm phụ trách để kiểm thử toàn diện.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Ôn tập toàn diện kiến trúc Amazon SageMaker và cơ chế lưu trữ tệp dữ liệu trên Amazon S3. <br> - Rà soát lại luồng truyền dữ liệu từ kho lưu trữ đến môi trường huấn luyện mô hình. | 20/07/2026 | 20/07/2026 |  |
| 3 | - Nghiên cứu sâu về SageMaker Processing Jobs để thiết lập các tác vụ xử lý dữ liệu hàng loạt tự động. <br> - Cấu hình SageMaker Endpoints để chuẩn bị cho việc cung cấp API suy luận thời gian thực. | 21/07/2026 | 21/07/2026 | |
| 4 | - Đưa mã nguồn huấn luyện và tái huấn luyện mô hình lên môi trường đám mây sử dụng các dịch vụ đã chuẩn bị. <br> - Thiết lập cơ chế tự động lưu trữ các artifact mô hình sau mỗi lần huấn luyện vào Amazon S3. | 22/07/2026 | 22/07/2026 |  |
| 5 | - Phối hợp với các thành viên trong nhóm để kết nối tầng Machine Learning với hệ thống Backend và Frontend của trang web xem phim. <br> - Kiểm tra luồng gọi API lấy danh sách phim gợi ý từ giao diện người dùng. | 23/07/2026 | 23/07/2026 |  |
| 6 | - Thực hiện kiểm thử toàn diện toàn bộ hệ thống từ đầu cuối đến đầu cuối trên môi trường đám mây. <br> - Ghi nhận các lỗi phát sinh trong quá trình truyền tải dữ liệu và tối ưu hóa độ trễ phản hồi của mô hình. | 24/07/2026 | 24/07/2026 | Hệ thống kiểm thử tích hợp |

### Kết quả đạt được tuần 7:

* **Làm chủ hạ tầng triển khai:** Ôn tập và ứng dụng thành công các công cụ Amazon S3, SageMaker Processing Jobs cùng SageMaker Endpoints vào việc vận hành mô hình trên đám mây.
* **Tự động hóa huấn luyện và lưu trữ:** Thiết lập hoàn chỉnh quy trình huấn luyện, tái huấn luyện và lưu trữ kết quả mô hình an toàn trên nền tảng AWS.
* **Tích hợp hệ thống thành công:** Phối hợp nhịp nhàng với đội ngũ phát triển web để kết nối mô hình gợi ý vào website xem phim, đảm bảo người dùng nhận được kết quả đề xuất trực quan ngay trên giao diện.
* Hoàn thành giai đoạn tích hợp hệ thống end-to-end, sẵn sàng cho việc kiểm tra khả năng chịu tải và giả lập sự cố ở tuần cuối cùng.