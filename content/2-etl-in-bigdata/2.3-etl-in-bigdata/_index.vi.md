---
title : "ETL trong Big data"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3. </b> "
---
### ETL
**ETL**, viết tắt của **Extract, Transform, Load**, là một quy trình quan trọng trong việc xử lý và chuẩn bị dữ liệu, đặc biệt đối với Big Data giúp tối ưu hóa dữ liệu cho phân tích, đảm bảo dữ liệu đầu vào đủ chất lượng cho quá trình phân tích về sau. Trong đó:
![bigdata](/images/3-etl-in-bigdata/etl.png)
  * **Extract (Trích xuất)**: 
    - Dữ liệu được trích xuất từ một hoặc nhiều nguồn dữ liệu, có thể gồm cơ sở dữ liệu truyền thống, hệ thống tệp, hoặc từ các thiết bị IoT, …..
    - Là bước đầu tiên và cơ bản nhất, yêu cầu tính chính xác cao để đảm bảo dữ liệu được thu thập đầy đủ và không bị biến đổi.
  * **Transform (Biến đổi)**: Dữ liệu trích xuất sau đó được làm sạch (loại bỏ dữ liệu nhiễu), chuẩn hóa, biến đổi, và lọc để đáp ứng nhu cầu và tiêu chuẩn cụ thể của dự án hoặc tổ chức.
  * **Load (Tải)**: Dữ liệu sau khi được biến đổi sẽ được tải vào kho dữ liệu hoặc hệ thống lưu trữ cuối, có thể là một Data Warehouse, Data Lake, hoặc Database phục vụ cho việc truy vấn phân tích về sau.

ETL giúp tối ưu hóa dữ liệu cho phân tích, đảm bảo dữ liệu đầu vào đủ chất lượng cho quá trình phân tích.

### Batch data & Streaming Data
Batch Data và Streaming Data là hai hướng tiếp cận chính trong việc xử lý và phân tích dữ liệu, sơ lược qua về 2 loại xử lý dữ liệu này:

#### Batch Data Processing (Xử lý dữ liệu theo lô)
  * **Khái niệm**: Là phương pháp mà dữ liệu được thu thập, lưu trữ và xử lý theo các lô (batch) hoặc đợt cố định (ví dụ theo lập lịch). Dữ liệu được xử lý trong một khoảng thời gian nhất định và thường đòi hỏi một lượng lớn dữ liệu để bắt đầu quá trình xử lý.
  * **Ứng dụng**: Thích hợp cho các tác vụ phức tạp cần xử lý dữ liệu lớn. (VD: phân tích kinh doanh, báo cáo, và các quy trình ETL truyền thống).
  * **Ví dụ**: Tính toán metrics kinh doanh hàng ngày, xử lý các giao dịch cuối ngày trong ngành ngân hàng, hoặc phân tích log truy cập website hàng tháng.

#### Streaming Data Processing (Xử lý dữ liệu theo luồng)
  * **Khái niệm**: Là phương pháp mà dữ liệu được xử lý ngay khi nó được tạo ra hoặc thu thập, gần như real-time. Xử lý Streaming Data cho phép phản ứng nhanh chóng đối với sự kiện và thông tin mới.
  * **Ứng dụng**: Phù hợp cho các ứng dụng yêu cầu thời gian phản hồi nhanh hoặc xử lý dữ liệu liên tục, như giám sát và phân tích dữ liệu thời gian thực, IoT, và xử lý sự kiện.
  * **Ví dụ**: Giám sát giao thông trong thời gian thực, phát hiện gian lận tài chính ngay lập tức, hoặc phân tích cảm xúc từ bài đăng trên mạng xã hội.

{{% notice note %}}
Có thể thấy, Batch processing thường xử lý lượng dữ liệu lớn với độ phức tạp đơn giản và độ trễ cao (do phụ thuộc vào lịch trình xử lý dữ liệu), trong khi đó, streaming processing xử lý phức tạp hơn để quản lý dữ liệu liên tục nhưng với quy mô nhỏ hơn tại mỗi thời điểm và độ trễ thấp (near realtime).
{{% /notice %}}


### Các công nghệ thường dùng trong Big Data
#### Apache Hadoop
  * Framework mã nguồn mở được viết bằng Java cho phép xử lý phân tán (distributed processing) các tập tin dữ liệu lớn trên các nhóm/cụm máy tính (clusters of computers) sử dụng các mô hình lập trình đơn giản; được thiết kế để mở rộng từ một máy chủ duy nhất sang hàng ngàn máy khác, mỗi máy cung cấp khả năng tính toán và lưu trữ cục bộ (local computation and storage).
  * **Đọc thêm**: [hadoop](https://www.simplilearn.com/tutorials/hadoop-tutorial)
  {{% notice info %}}
  Về **Hadoop** thì chỉ cần học qua về hệ sinh thái cơ bản Hadoop (HDFS, MapRedure, YARN), không cần quá deep dive.
  {{% /notice %}}

#### Apache Spark
  * Framework mã nguồn mở, dành cho việc xử lý và phân tích dữ liệu lớn (Big Data). Được thiết kế để nhanh chóng xử lý dữ liệu lớn thông qua việc thực hiện tính toán **in-memory (trên RAM)**, với tốc độ xử lý dữ liệu có thể nhanh hơn 100 lần so với MapReduce. và có thể chạy trên cả cơ sở hạ tầng on-premise lẫn các dịch vụ on-cloud.
  * Không có hệ thống file của riêng mình (**không phụ thuộc vào bất cứ một hệ thống file nào**), nó sử dụng hệ thống file khác như: HDFS, Cassandra, S3,…. 
  * Hỗ trợ **nhiều kiểu định dạng file** khác nhau (text, csv, json…)
  * Xử lý dữ liệu: theo lô (**batch dat**a) và theo thời gian thực (**streaming data**).
  * Hỗ trợ ngôn ngữ: Java, Scala, **Python** và R.
  * **Đọc thêm**: [spark](https://www.youtube.com/watch?v=znBa13Earms)

#### Apache Kafka
  * Nền tảng mã nguồn mở được sử dụng cho việc xử lý luồng dữ liệu **realtime**, phát triển bởi LinkedIn và hiện tại được quản lý bởi Apache Software Foundation. Trong ngữ cảnh của Big Data, Kafka được biết đến như một hệ thống truyền tải dữ liệu hiệu suất cao, đáng tin cậy, có khả năng mở rộng và linh hoạt, thích hợp cho việc xây dựng các ứng dụng xử lý dữ liệu thời gian thực.
  * Ứng dụng: Xử lý dữ liệu thời gian thực, ghi lại log/event, truyền thông giữa các dịch vụ, tích hợp dữ liệu và ETL dữ liệu realtime,...
  * **Đọc thêm**: [kafka](https://www.youtube.com/watch?v=PzPXRmVHMxI/) 

----------------------
**Ví dụ - Xét ví dụ đối với xử lý on-prem**: Về ETL dữ liệu lớn realtime có sử dụng các công nghệ thường dùng dành cho BigData như Apache Hadoop, Apache Spark, Apache Kafka như sau:
  1. Extract:
     * Dùng **Kafka** cho việc thu thập/trích xuất dữ liệu realtime
  2. Transform:
     * Dùng **Spark Streaming** để xử lý dữ liệu từ Kafka. Các dữ liệu sẽ được làm sạch, biến đổi (ví dụ: lọc bỏ các giá trị trống) và chuẩn bị cho việc phân tích.
     * Biến đổi dữ liệu: Dữ liệu sau khi được làm sạch có thể được tổng hợp (ví dụ: tính tổng, trung bình theo các tiêu chí nào đó) và chuẩn bị cho việc lưu trữ.
  3. Load: 
     * Lưu trữ dữ liệu sau khi dữ liệu đã được xử lý bởi Spark sẽ được lưu trữ trong **Hadoop HDFS**, cho phép lưu trữ dữ liệu lớn một cách hiệu quả và kinh tế.
     * Lưu trữ dữ liệu phân tích: Dữ liệu tổng hợp có thể được lưu trữ dưới dạng tệp Parquet hoặc ORC, tối ưu hóa cho việc truy vấn phân tích.
Kết thúc quá trình ETL dữ liệu, bạn sẽ thành công trích xuất dữ liệu realtime, và thực hiện biến đổi dữ liệu rồi lưu vào hệ thống lưu trữ đích (ở ví dụ trên thì là hệ lưu trữ và quản lý dữ liệu phân tán - HDFS)
