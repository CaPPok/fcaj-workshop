---
title: "Blog 2"
date: 2026-07-29
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# AWS FAULT INJECTION SERVICE – CHỦ ĐỘNG TẠO LỖI ĐỂ KIỂM TRA ĐỘ ỔN ĐỊNH CỦA HỆ THỐNG

Tuần qua, mình có tìm hiểu về việc làm thế nào để triển khai và vận hành ứng dụng sao cho hoạt động ổn định. Tuy nhiên, khi tìm hiểu thêm về các nguyên tắc của AWS Well-Architected Framework, mình biết đến một khái niệm là Chaos Engineering – chủ động tạo ra các tình huống lỗi để kiểm tra xem hệ thống có thực sự đủ khả năng phục hồi hay không. Để hỗ trợ việc này, AWS cung cấp AWS Fault Injection Service.

Đây là một dịch vụ giúp tạo các thử nghiệm có kiểm soát trên hạ tầng AWS nhằm đánh giá khả năng chịu lỗi của hệ thống trước những sự cố như mất kết nối mạng, tăng tải CPU hoặc dừng một EC2 Instance. Điểm mình thấy hay là các thử nghiệm đều được thực hiện theo một kịch bản đã định nghĩa trước, thay vì tạo lỗi một cách ngẫu nhiên.

## AWS FIS có thể làm gì?

Sau khi tìm hiểu, mình thấy AWS FIS hỗ trợ nhiều loại thử nghiệm như:

- Dừng hoặc khởi động lại EC2 Instance.
- Tăng mức sử dụng CPU trên EC2.
- Giả lập độ trễ hoặc mất kết nối mạng.
- Thử nghiệm với Amazon ECS hoặc Amazon EKS.
- Kiểm tra phản ứng của Auto Scaling khi một Instance gặp sự cố.

{{% notice note %}}
Thông qua các thử nghiệm này, nhóm phát triển có thể đánh giá xem hệ thống có tự phục hồi đúng như mong đợi hay không.
{{% /notice %}}

## Fault Injection Experiment

Để hiểu rõ hơn, mình thử tìm hiểu cách tạo một thử nghiệm đơn giản trên EC2.

**Bước 1:** Truy cập AWS Console và tìm AWS Fault Injection Service.

**Bước 2:** Chọn Create experiment template.

Template sẽ mô tả toàn bộ thử nghiệm, bao gồm tài nguyên, hành động và điều kiện dừng.

**Bước 3:** Chọn tài nguyên mục tiêu.

Ví dụ: Một EC2 Instance trong môi trường Development hoặc Testing.

{{% notice tip %}}
Theo mình, không nên thử nghiệm trực tiếp trên môi trường Production khi chưa đánh giá kỹ tác động.
{{% /notice %}}

**Bước 4:** Chọn hành động.

Ví dụ:

- Stop EC2 Instance.
- Reboot EC2 Instance.
- Stress CPU.

**Bước 5:** Thiết lập Stop Conditions. Đây là bước mình thấy khá quan trọng.

Có thể cấu hình để thử nghiệm tự dừng nếu CloudWatch Alarm chuyển sang trạng thái ALARM, giúp hạn chế ảnh hưởng nếu hệ thống gặp vấn đề ngoài dự kiến.

**Bước 6:** Review và tạo Experiment Template.

**Bước 7:** Chạy thử nghiệm.

Sau khi bắt đầu, AWS sẽ thực hiện các hành động theo đúng kịch bản và hiển thị trạng thái của từng bước trên Dashboard.

## Ưu điểm

Sau khi tìm hiểu, mình thấy AWS FIS có một số ưu điểm như:

- Giúp đánh giá khả năng chịu lỗi của hệ thống trong môi trường thực tế.
- Hỗ trợ nhiều loại tài nguyên và nhiều kịch bản thử nghiệm.
- Có thể kết hợp với CloudWatch để tự động dừng thử nghiệm nếu phát hiện sự cố nghiêm trọng.
- Không cần tự xây dựng các script để tạo lỗi.
- Phù hợp để kiểm tra các cơ chế như Auto Scaling, Load Balancing hoặc Disaster Recovery.

{{% notice note %}}
Việc chủ động kiểm tra khả năng phục hồi sẽ giúp phát hiện các điểm yếu trước khi xảy ra sự cố thật.
{{% /notice %}}

## Một số điểm cần lưu ý

Bên cạnh những ưu điểm trên, mình cũng thấy có một vài điều cần cân nhắc.

AWS FIS không nên được sử dụng trực tiếp trên môi trường Production nếu chưa có kế hoạch và quy trình kiểm soát phù hợp. Ngoài ra, để các kết quả có ý nghĩa, hệ thống cần được giám sát bằng các công cụ như Amazon CloudWatch hoặc AWS X-Ray để có thể quan sát tác động của từng thử nghiệm.

Việc thiết kế kịch bản thử nghiệm cũng cần bám sát các tình huống có thể xảy ra trong thực tế, thay vì tạo lỗi một cách ngẫu nhiên.

## Khi nào nên sử dụng?
Theo mình, AWS FIS sẽ phù hợp trong các trường hợp như:
- Kiểm tra khả năng tự phục hồi của hệ thống.
- Đánh giá Auto Scaling hoặc Load Balancer.
- Kiểm tra quy trình Disaster Recovery.
- Thử nghiệm trước khi triển khai các hệ thống quan trọng.
- Thực hành Chaos Engineering trong môi trường Development hoặc Testing.

## Kết luận

Sau khi tìm hiểu, mình thấy AWS Fault Injection Service là một service khá thú vị. Thay vì chỉ tập trung ngăn ngừa lỗi, AWS khuyến khích người dùng chủ động tạo ra các tình huống lỗi có kiểm soát để đánh giá khả năng phục hồi của hệ thống.

Đây là một cách tiếp cận mà trước đây mình chưa từng nghĩ đến. Nếu có cơ hội làm việc với các hệ thống lớn hoặc yêu cầu tính sẵn sàng cao, mình nghĩ AWS FIS sẽ là một công cụ đáng để tìm hiểu thêm.

Nếu anh/chị hoặc các bạn đã từng sử dụng AWS FIS hoặc có kinh nghiệm về Chaos Engineering, rất mong được nghe thêm các tình huống thực tế để cùng trao đổi.

## Tài liệu tham khảo
1. [AWS Fault Injection Service – Features](https://aws.amazon.com/fis/features/)
2. [AWS Well-Architected Framework – Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/)
3. [AWS Fault Injection Service Pricing](https://aws.amazon.com/fis/pricing/)
4. [AWS Documentation – AWS Fault Injection Service](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html)