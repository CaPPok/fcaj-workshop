---
title: "Event 2"
date: 2026-7-30
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “Event Day - 11/07/2026”

### Mục Đích Của Sự Kiện

Đây là sự kiện trao đổi giao lưu hàng tuần của chương trình FCAJ, diễn ra vào mỗi thứ 7. Đây cũng là event thứ hai mà em tham dự kể từ khi gia nhập FCAJ. 

- Trận chung kết cuộc thi **Cloud Architect**.
- Chia sẻ dịch vụ của AWS.
- Cách triển khai và đánh giá dự án real-time.
- Giới thiệu về chứng chỉ **AWS Cloud Practitioner**.

### Danh Sách Diễn Giả

Danh sách diễn giả trong sự kiện bao gồm : 

- **Anh Thịnh**, hiện là DevOps/DevSecOps/Cloud Engineer - Styl Solutions - First Cloud AI Journey chia sẻ về **Securing Your Web Apps With AWS Security Agent**.
- **Anh Nguyễn Huỳnh Sơn** chia sẻ về **SLA and Monitoring**.
- **Anh Ngô Lê Tấn Huy** giới thiệu về **AWS Cloud Practitioner**.

### Nội Dung Nổi Bật

#### Cuộc thi Cloud Architect

- Tổ chức trận chung kết cuộc thi **Cloud Architect**.
- Xem được bộ câu hỏi về các dịch vụ AWS.
- Giải quyết các câu hỏi về tình huống thực tế khi triển khai lên Cloud.

#### Securing Your Web Apps With AWS Security Agent

- **Tổng quan về bảo mật:** Các phương pháp kiểm thử bảo mật truyền thống thường đối mặt với nhiều rào cản lớn như thời gian thực hiện thủ công kéo dài hàng tuần, chi phí nhân sự chuyên gia cao, tính không đồng nhất phụ thuộc vào kỹ năng của người kiểm thử.
- **Giải pháp AI Agent:** Được hỗ trợ bởi Amazon Bedrock, agent tự trị này có khả năng lên kế hoạch và thực thi các tác vụ bảo mật mà không cần sự can thiệp của con người. Công cụ này bao phủ toàn bộ vòng đời phát triển từ đánh giá thiết kế, bảo mật mã nguồn đến kiểm thử xâm nhập chủ động, đồng thời vượt trội hơn các chatbot LLM thông thường nhờ khả năng xác thực lỗ hổng qua các thao tác tấn công thực tế.
- **Các hạn chế quan trọng:** Agent vẫn gặp phải những điểm nghẽn như các rào cản xác thực, khó khăn trong việc phát hiện các lỗi logic và gian lận nghiệp vụ nếu thiếu ngữ cảnh sâu, cũng như việc tích lũy giờ tác vụ rất nhanh đối với các ứng dụng phức tạp đòi hỏi phải có sự giám sát chặt chẽ.

#### SLA and Monitoring

- **Tổng quan về SLA và Quản lý rủi ro:** SLA - Service Level Agreement là cam kết dịch vụ chính thức giữa nhà cung cấp và khách hàng, đóng vai trò cốt lõi trong việc tạo lập kỳ vọng rõ ràng, trách nhiệm giải trình, quản lý rủi ro và đo lường hiệu suất. Giám sát nằm trong quy trình quản lý rủi ro nhằm phát hiện sớm các sự cố trước khi chúng tác động đến SLA hay tạo ra phàn nàn từ khách hàng, xoay quanh vòng lặp: Nhận diện rủi ro -> Giám sát tín hiệu -> Phản hồi -> Cải thiện.
- **Khoảng cách giữa "Hạ tầng khỏe mạnh" và "Trải nghiệm người dùng":** Một cạm bẫy lớn trong giám sát là quan niệm "hạ tầng khỏe mạnh đồng nghĩa với người dùng hạnh phúc", trong khi thực tế các chỉ số phần cứng riêng lẻ không thể kể hết toàn bộ câu chuyện. Do đó, hệ thống cần giám sát từ tháp cấu trúc nhiều tầng để hiểu rõ thực tế người dùng đang làm gì thay vì chỉ nhìn vào các server.
- **Luồng cảnh báo tự động và bài học thực tế:** Dòng chảy từ chỉ số tùy chỉnh qua **CloudWatch Alarm**, phát tán qua SNS Topic đến các kênh thông báo như Email/Slack giúp đội ngũ kỹ thuật phản ứng kịp thời trước khi nhận khiếu nại.

#### **Inside The Exam: AWS Cloud Practitioner**

- Giới thiệu về cách lấy chứng chỉ **AWS Cloud Practitioner**.
- Nói về cấu trúc bài kiểm tra.
- Chia sẻ tips, tricks và các nguồn tài liệu học tập hữu ích.

### Những gì học được

- **Nâng cao tư duy bảo mật ứng dụng:** Hiểu rõ cách ứng dụng công nghệ tự trị dựa trên AI như AWS Security Agent để tối ưu hóa vòng đời phát triển, từ đánh giá thiết kế, quét mã nguồn cho đến tự động kiểm thử xâm nhập với chi phí và hiệu quả tối ưu.
- **Tư duy giám sát toàn diện từ SLA:** Nhận thức rõ sự khác biệt cốt lõi giữa "hạ tầng khỏe mạnh" và "trải nghiệm thực tế của người dùng", từ đó biết cách thiết lập hệ thống cảnh báo từ tầng business và customer experience để phản ứng kịp thời trước khi sự cố ảnh hưởng đến khách hàng.
- **Định hướng chứng chỉ quốc tế:** Nắm bắt cấu trúc đề thi, kinh nghiệm ôn tập cũng như các tài liệu hữu ích để chuẩn bị cho hành trình chinh phục chứng chỉ AWS Cloud Practitioner.

### Trải nghiệm trong event

Đây là một buổi event mang lại cho em rất nhiều kiến thức thực chiến và những góc nhìn mới mẻ, đặc biệt là khi được lắng nghe những chia sẻ chuyên sâu từ các anh chị đi trước trong ngành Cloud và DevSecOps.

#### Không khí hào hứng và chuyên nghiệp

Sự kiện diễn ra trong bầu không khí vô cùng sôi nổi, từ phần tranh tài gay cấn của các đội thi trong trận chung kết Cloud Architect cho đến các phiên chia sẻ kiến thức kỹ thuật đầy chiều sâu. Mọi thứ đều được chuẩn bị và vận hành rất mượt mà nhờ sự tâm huyết của ban tổ chức và đội ngũ mentor FCAJ.

#### Tiếp thu kiến thức thực tế

Các chủ đề được trình bày không chỉ dừng lại ở lý thuyết sách vở mà còn lồng ghép rất nhiều bài học xương máu từ thực tế doanh nghiệp. Việc được tiếp cận với các công nghệ tiên tiến như **AI Security Agents** hay hiểu đúng bản chất của **SLA and Monitoring** giúp em vỡ lẽ ra rất nhiều điều, định hình rõ ràng hơn con đường phát triển kỹ năng trong tương lai.

#### Kết nối và mở rộng tầm nhìn

Event tiếp tục là cầu nối tuyệt vời để em được giao lưu, học hỏi cùng cộng đồng những người đam mê công nghệ. Những lời khuyên về lộ trình học tập, kinh nghiệm làm việc và định hướng chinh phục các chứng chỉ quốc tế như **AWS Cloud Practitioner** thực sự là nguồn động lực lớn đối với một thành viên mới như em.

#### Một số hình ảnh khi tham gia sự kiện

![Event 3](/images/4-EventParticipated/event-3.jpg)
![Event 4](/images/4-EventParticipated/event-4.jpeg)