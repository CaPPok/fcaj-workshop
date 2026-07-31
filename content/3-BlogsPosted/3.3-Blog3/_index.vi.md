---
title: "Blog 3"
date: 2026-07-29
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# TÌM HIỂU AWS RESOURCE EXPLORER – TÌM KIẾM TÀI NGUYÊN TRÊN AWS DỄ DÀNG HƠN

Trong quá trình học AWS, mình nhận ra khi số lượng dịch vụ và tài nguyên ngày càng nhiều thì việc quản lý cũng trở nên khó hơn. Có những lúc mình nhớ đã tạo một Lambda Function hoặc một EC2 Instance nhưng lại không nhớ chính xác ở Region nào hoặc tên đầy đủ là gì.

Sau khi tìm hiểu tài liệu của AWS, mình biết đến AWS Resource Explorer. Đây là một service cho phép tìm kiếm tài nguyên trên AWS thông qua một giao diện thống nhất, thay vì phải mở từng dịch vụ để tìm. Resource Explorer có thể lập index các tài nguyên trong tài khoản và hỗ trợ tìm kiếm theo tên, loại tài nguyên hoặc Region.

## AWS Resource Explorer có thể làm gì?

Sau khi đọc tài liệu và thử sử dụng, mình thấy Resource Explorer hỗ trợ khá nhiều trường hợp thực tế như:

- Tìm nhanh EC2 Instance, S3 Bucket, Lambda Function hoặc DynamoDB Table.
- Tìm tài nguyên theo Region.
- Tìm tài nguyên theo tên hoặc ARN.
- Kiểm tra xem tài nguyên đã bị xóa hay vẫn còn tồn tại.
- Hỗ trợ quản lý khi tài khoản có nhiều Region hoặc nhiều project.

{{% notice note %}}
Service này đặc biệt hữu ích khi bắt đầu có nhiều môi trường như Development, Testing và Production.
{{% /notice %}}

## Thử sử dụng AWS Resource Explorer

Để hiểu rõ hơn, mình thử cấu hình theo hướng dẫn của AWS.

**Bước 1:** Truy cập AWS Console và tìm AWS Resource Explorer.

**Bước 2:** Chọn Create Index.

Index giúp AWS thu thập thông tin về các tài nguyên trong tài khoản. Thông thường chỉ mất vài phút để hoàn tất.

**Bước 3:** Tạo Default View.

View sẽ xác định phạm vi tài nguyên được phép tìm kiếm. Có thể giới hạn theo Region hoặc cho phép tìm kiếm trên nhiều Region.

**Bước 4:** Bắt đầu tìm kiếm.

Ví dụ mình nhập:

```text
resourcetype:ec2:instance
```

để hiển thị toàn bộ EC2 Instance.

Hoặc tìm theo tên:

```text
movie-api
```

AWS sẽ trả về những tài nguyên có tên hoặc metadata phù hợp.

## Ưu điểm

Sau khi sử dụng thử, mình thấy Resource Explorer có một số ưu điểm như:

- Không cần mở từng dịch vụ để tìm tài nguyên.
- Hỗ trợ tìm kiếm trên nhiều Region.
- Giao diện đơn giản, dễ sử dụng.
- Có thể tìm kiếm bằng nhiều điều kiện khác nhau.
- Phù hợp khi số lượng tài nguyên ngày càng nhiều.

{{% notice tip %}}
Theo mình, nếu đang học AWS thì có thể chưa cảm nhận rõ lợi ích. Nhưng khi triển khai nhiều project hoặc tham gia quản lý một tài khoản AWS dùng chung cho nhiều nhóm, việc tìm kiếm tài nguyên sẽ nhanh hơn rất nhiều.
{{% /notice %}}

## Một số điểm cần lưu ý

Bên cạnh những ưu điểm trên, mình cũng thấy có một vài điều cần lưu ý.

Trước hết, Resource Explorer cần được tạo Index trước khi sử dụng. Nếu chưa có Index thì sẽ không thể tìm kiếm tài nguyên. Ngoài ra, kết quả tìm kiếm còn phụ thuộc vào quyền IAM của người dùng. Nếu IAM User hoặc IAM Role không có quyền xem một tài nguyên nào đó thì Resource Explorer cũng sẽ không hiển thị tài nguyên đó.

{{% notice note %}}
Đây là công cụ hỗ trợ tìm kiếm và quản lý tài nguyên, không thay thế các dịch vụ quản trị hoặc giám sát như AWS Config hay CloudWatch.
{{% /notice %}}

## Khi nào nên sử dụng?

Theo mình, Resource Explorer sẽ phù hợp khi:

- Quản lý nhiều dịch vụ AWS trong cùng một tài khoản.
- Làm việc với nhiều Region.
- Muốn tìm nhanh một tài nguyên mà không nhớ chính xác vị trí.
- Kiểm tra tài nguyên còn tồn tại trước khi dọn dẹp hoặc tối ưu chi phí.

## Kết luận
Sau khi tìm hiểu, mình thấy AWS Resource Explorer là một service khá đơn giản nhưng lại rất hữu ích trong quá trình quản lý tài nguyên trên AWS. Thay vì phải mở từng dịch vụ rồi tìm kiếm thủ công, chỉ cần một giao diện duy nhất là đã có thể tra cứu hầu hết các tài nguyên trong tài khoản.

Mình nghĩ đây là một service đáng thử, đặc biệt khi số lượng tài nguyên bắt đầu nhiều hơn hoặc khi làm việc trong các dự án có nhiều môi trường và nhiều Region.

## Tài liệu tham khảo
1. [AWS Documentation – AWS Resource Explorer](https://docs.aws.amazon.com/resource-explorer/latest/userguide/welcome.html)
2. [Getting Started with AWS Resource Explorer](https://docs.aws.amazon.com/resource-explorer/latest/userguide/getting-started.html)
3. [Search syntax for AWS Resource Explorer](https://docs.aws.amazon.com/resource-explorer/latest/userguide/using-search-query.html)