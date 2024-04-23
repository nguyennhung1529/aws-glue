---
title : "Data Models"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1. </b> "
---

Trong lĩnh vực data, mô hình dữ liệu (data model) đóng vai trò quan trọng trong việc tổ chức, lưu trữ và quản lý dữ liệu. Có nhiều loại mô hình dữ liệu, nhưng một số phổ biến bao gồm:

#### 1.Mô hình quan hệ (Relational Model)
  * Được sử dụng rộng rãi trong các hệ thống quản trị cơ sở dữ liệu quan hệ (RDBMS).
  * Dữ liệu được tổ chức thành các bảng, với mỗi bảng gồm hàng (dữ liệu) và cột (thuộc tính).
  * Các bảng có thể liên kết với nhau thông qua các khóa.
  ![datamodel](/images/data-models/Relational-model.png)

#### 2. Mô hình dữ liệu phi quan hệ (NoSQL)
  * Thích hợp cho dữ liệu không cấu trúc hoặc bán cấu trúc, và khi cần khả năng mở rộng ngang.
  * Bao gồm một số loại như: key-value store, document store, wide-column store, và graph databases.
  * Ví dụ: MongoDB / AWS DynamoDB (document store), Cassandra (wide-column store), Neo4j / Amazon Neptune (graph database).
  ![datamodel](/images/data-models/nosql-model.png)

#### 3. Mô hình đa chiều (Multidimensional Model)
  * Thường được sử dụng trong data warehousing và business intelligence (BI) để hỗ trợ truy vấn và phân tích dữ liệu nhanh chóng.
  * Dữ liệu được tổ chức thành các cube, với mỗi chiều (dimension) đại diện cho một thuộc tính dữ liệu, và các cell trong cube chứa các giá trị dữ liệu.
  ![datamodel](/images/data-models/dimension-model.png)

#### 4. Mô hình đồ thị (Graph Model)
  * Sử dụng đồ thị (nodes và edges) để mô hình hóa dữ liệu và mối quan hệ giữa chúng.
  * Phù hợp với các ứng dụng mà mối quan hệ giữa các đối tượng là quan trọng, như mạng xã hội, hệ thống đề xuất, và phân tích liên kết.
  ![datamodel](/images/data-models/graph-model.png)

Trong Big Data, do tính chất đa dạng và lớn về khối lượng dữ liệu, tùy thuộc vào yêu cầu cụ thể của dự án mà có thể sẽ thường chọn các loại data models sau:
  * Mô hình phi quan hệ (NoSQL): Do khả năng mở rộng ngang và linh hoạt trong việc lưu trữ dữ liệu không cấu trúc hoặc bán cấu trúc, NoSQL thường được yêu thích lựa chọn trong các ứng dụng Big Data.
  * Mô hình đồ thị (Graph Model): Dành cho các dự án liên quan đến phân tích mạng xã hội, đề xuất nội dung, hoặc các ứng dụng cần đến việc hiểu rõ mối quan hệ giữa các đối tượng.