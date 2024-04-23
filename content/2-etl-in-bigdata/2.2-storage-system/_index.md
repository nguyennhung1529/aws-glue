---
title : "Hệ thống lưu trữ"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2.  </b> "
---

Việc chọn loại hệ thống lưu trữ sẽ phụ thuộc vào data models, lựa chọn hệ thống lưu trữ phù hợp là yếu tố quan trọng để đảm bảo hiệu suất và khả năng mở rộng, đặc biệt là đối với Big Data. Dưới đây là một số loại hệ thống lưu trữ Big Data phổ biến:
  * **Hệ thống lưu trữ phân tán (HDFS)**:
    - **Đặc điểm**: Là hệ thống lưu trữ dựa trên mô hình hệ thống file phân tán được thiết kế để chạy trên phần cứng thông thường. HDFS có khả năng lưu trữ dữ liệu với khối lượng lớn và hỗ trợ việc sao chép và phân tán dữ liệu trên nhiều máy để đảm bảo độ tin cậy và khả năng phục hồi.
    - **Ứng dụng**: Phù hợp cho việc lưu trữ và xử lý dữ liệu không cấu trúc hoặc bán cấu trúc với khối lượng lớn.
  * **NoSQL Databases**
    - **Đặc điểm**: Là loại cơ sở dữ liệu không tuân thủ theo mô hình cơ sở dữ liệu quan hệ truyền thống, được thiết kế để lưu trữ dữ liệu không cấu trúc hoặc bán cấu trúc với khả năng mở rộng cao. 
    - Ví dụ: MongoDB, Cassandra, HBase, Couchbase, AWS DynamoDB, ....
    - **Ứng dụng**: Thích hợp cho các ứng dụng cần độ mở rộng cao và thời gian phản hồi nhanh, như web và ứng dụng di động, dữ liệu thời gian thực và IoT.
  * **Data Lakes**: 
    - Cung cấp khả năng lưu trữ dữ liệu thô ở quy mô lớn, bao gồm dữ liệu cấu trúc và không cấu trúc; Data lake này có thể là một hệ thống lưu trữ on-prem hoặc một dịch vụ Data Lake on-cloud.
    - Ví dụ: Hệ thống data lake on-premises, AWS S3, Google Cloud Storage, Azure Data Lake Storage, ...

Bên cạnh các loại hệ thống lưu trữ trên, còn có hệ thống lưu trữ điển hình khác đó là **Data Warehouses** - Cho phép lưu trữ dữ liệu đã được cấu trúc hóa và chuẩn hóa, thích hợp cho việc phân tích và báo cáo. Nếu Data Lake phù hợp với việc lưu trữ và phân tích dữ liệu Big Data thô và không cấu trúc (dữ liệu input); thì Data Warehouse tối ưu cho việc lưu trữ, truy vấn, và phân tích dữ liệu đã được cấu trúc hóa (output dữ liệu sau khi đã được tranform thành các tập có cấu trúc).

{{% notice info %}}
Phần này mình sẽ không giới thiệu về **Data Lakehouse**, vì hiện nay Data Lakehouse vẫn còn là một khái niệm tương đối mới và đang phát triển, vì vậy các công nghệ và công cụ hỗ trợ còn đang trong quá trình hoàn thiện => rủi ro và thách thức trong việc triển khai và bảo trì. \
\
Tuy nhiên, sơ lược thì **Data Lakehouse = Data Lake + Data Warehouse**. Lấy ưu điểm của cả Data Lake và Data Warehouse, cung cấp cả khả năng lưu trữ dữ liệu thô lớn của Data Lake và tính năng quản lý và truy vấn dữ liệu cấu trúc hóa của Data Warehouse.
{{% /notice %}}