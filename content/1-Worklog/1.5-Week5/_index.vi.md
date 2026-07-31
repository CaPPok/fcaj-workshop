---
title: "Worklog Tuần 5"
date: 2026-07-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

- Xây dựng thuật toán lai kết hợp các mô hình để khắc phục các nhược điểm đơn lẻ.
- Thiết lập cơ chế kiểm định chất lượng tự động thông qua Promotion Gate.
- Đánh giá hiệu suất mô hình bằng các chỉ số định lượng chuyên sâu.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Nghiên cứu phương pháp kết hợp kết quả gợi ý giữa mô hình Collaborative Filtering và các mô hình thành phần khác. <br> - Xây dựng thuật toán lai sử dụng phương pháp Weighted Reciprocal Rank Fusion. | 06/07/2026 | 06/07/2026 | <https://www.paradedb.com/learn/search-concepts/reciprocal-rank-fusion>, <https://learn.microsoft.com/en-us/azure/search/hybrid-search-ranking> |
| 3 | - Tích hợp thuật toán lai vào hệ thống để xử lý các trường hợp thiếu dữ liệu lịch sử. <br> - Kiểm tra khả năng mở rộng không gian gợi ý và đa dạng hóa danh mục phim. | 07/07/2026 | 07/07/2026 |  |
| 4 | - Phát triển script đánh giá mô hình. <br> - So sánh hiệu suất giữa mô hình lai và mô hình cơ sở phổ biến. | 08/07/2026 | 08/07/2026 |  |
| 5 | - Xây dựng cơ chế Promotion Gate để tự động kiểm duyệt phiên bản mô hình mới. <br> - Lập quy tắc kiểm tra số lượng người dùng được đánh giá. | 09/07/2026 | 09/07/2026 |  |
| 6 | - Kiểm tra toàn bộ quy trình tự động hóa cập nhật mô hình trên môi trường thử nghiệm. <br> - Tổng hợp các báo cáo hiện thực và đánh giá mô hình. | 10/07/2026 | 10/07/2026 |  |

### Kết quả đạt được tuần 5:

* **Hoàn thiện thuật toán lai:** Xây dựng thành công phương pháp kết hợp giúp giải quyết triệt để sự cố thiếu dữ liệu lịch sử của người dùng mới, đồng thời nâng cao độ chính xác và đa dạng hóa danh mục gợi ý.
* **Đánh giá định lượng hiệu quả:** Thiết lập thành công các chỉ số đo lường hiệu suất, chứng minh mô hình lai đạt được độ chính xác cao và vượt trội hơn so với mô hình cơ sở.
* **Tự động hóa kiểm định:** Xây dựng cơ chế Promotion Gate giúp hệ thống chỉ chấp nhận đưa vào sử dụng các phiên bản mô hình mới khi vượt qua các ngưỡng tiêu chuẩn về chất lượng.