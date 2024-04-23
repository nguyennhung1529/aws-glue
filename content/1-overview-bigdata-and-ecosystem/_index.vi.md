---
title : "Tổng quan về Big Data và Ecosystem"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Big Data** là thuật ngữ dùng để mô tả khối lượng dữ liệu rất lớn, phức tạp tới mức các công cụ xử lý dữ liệu truyền thống không có khả năng thu thập, lưu trữ, quản lý và phân tích/xử lý trong một khoảng thời gian hợp lý. Big Data không chỉ đơn giản về khối lượng dữ liệu lớn mà còn về tốc độ dữ liệu được tạo ra và đa dạng của dữ liệu đó (có cấu trúc, không cấu trúc và bán cấu trúc).

![bigdata](/images/1-overview-bigdata-and-ecosystem/bigdata.png)

{{% notice note %}}
Ví dụ về ứng dụng của Big Data trong lĩnh vực ngân hàng như phân tích rủi ro và gian lận, tối ưu hóa danh mục đầu tư từ lượng lớn dữ liệu thu thập từ thị trường tài chính, … Hoặc trong lĩnh vực marketing có ứng dụng sử lý bigdata cho việc nhận diện hành vi khách hàng giúp cá nhân hóa dịch vụ và sản phẩm, hoặc ơhân tích dữ liệu từ nhiều nguồn để tối ưu chiến dịch quảng cáo, ….
\
Ngoài ra còn nhiều ngành đang áp dụng Big Data như nông nghiệp, giáo dục… => cung cấp insight tốt về dữ liệu => hỗ trợ ra quyết định nhanh chóng và chính xác.
{{% /notice %}}

Big Data thường được mô tả thông qua ba "V":
  * **Volume (Khối lượng)**: Lượng dữ liệu lớn, thường là petabytes hoặc exabytes được tạo ra từ các nguồn khác nhau như doanh nghiệp, máy móc, thiết bị IoT, truyền thông xã hội, v.v.
  * **Velocity (Tốc độ)**: Tốc độ nhanh chóng mà dữ liệu được tạo ra và cần phải được thu thập, xử lý. Trong nhiều trường hợp, dữ liệu cần được xử lý nhanh chóng để khai thác sử dụng.
  * **Variety (Đa dạng)**: Sự đa dạng về loại dữ liệu, bao gồm dữ liệu cấu trúc (Excel, dữ liệu trong các bảng trong DB, …), không cấu trúc (hình ảnh, video, pdf, …) và bán cấu trúc (XML, HTLM, …).

![bigdata](/images/1-overview-bigdata-and-ecosystem/what-is-big-data.png)

Ngoài ra, hai "V" khác cũng thường được đề cập:
  * **Veracity (Độ chính xác)**: Độ tin cậy và chính xác của dữ liệu (có thể bị ảnh hưởng bởi dữ liệu nhiễu, dữ liệu không đầy đủ hoặc lỗi).
  * **Value (Giá trị)**: Khả năng trích xuất thông tin có ích và có giá trị từ dữ liệu.
 
{{% notice info %}}
**Bao nhiêu dữ liệu mới đủ gọi là 'big'?**\
Không có một ngưỡng cụ thể nào vì nó phụ thuộc vào khả năng khai thác và xử lý của công nghệ hiện tại và nhu cầu cụ thể của mỗi tổ chức. Một lượng dữ liệu có thể được coi là "lớn" ở thời điểm này có thể không còn phù hợp trong vài năm sau do sự phát triển của công nghệ và kỹ thuật xử lý dữ liệu. Tuy nhiên, một cách tổng quát, khi dữ liệu bắt đầu tính bằng petabytes trở lên và không thể được xử lý một cách hiệu quả bằng cơ sở dữ liệu truyền thống, nó thường được coi là Big Data.
{{% /notice %}}