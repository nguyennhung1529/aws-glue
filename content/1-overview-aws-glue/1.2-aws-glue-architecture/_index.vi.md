---
title : "AWS Glue Architecture"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 1.2. </b> "
---
We define jobs in AWS Glue to accomplish the work that is required to extract, transform and load data from a data source to a data target. So if we talk about the workflow, the first step here is we define a crawler to populate our AWS data catalog with metadata and table definitions. We point our crawler at a data source post and the crawler creates table definitions in the data catalog. In addition to table definitions, the data catalog contains other metadata that is required to define ETL jobs. we use this metadata when we define a job to transform our data in the second step. AWS Glue can generate a script to transform our data or we can also provide the script in the AWS Glue console. In the third step, we can run our job on demand or we can set it up to start when a specified trigger occurs. The trigger can be a time-based schedule or an event. Finally, when our job runs, a script extracts data from our data source, transforms the data, and loads it into our target. The script runs in an Apache Spark environment in AWS Glue.

![AWSGlue](/images/1-overview-aws-glue/aws-glue-architecture.png)

  * **Data Catalog:** It is the persistent metadata store in AWS Glue. It contains table definitions, job definitions, etc. AWS Glue has one data catalog per region.
  * **Database:** It is a set of associated data catalog table definitions organized into a logical group in the AWS group. 
  * **Table:** It contains the name of columns, data types, definitions, and other metadata about a base dataset.
  * **Crawler:** It is a program that connects to our data store. Maybe a source or a target progresses through a prioritized list of classifiers to determine the schema for our data and then it creates metadata tables in the data catalog. 
  * **Classifier:** It determines the schema of our data. AWS Glue provides classifiers for common file types such as CSV, JSON, etc. It also provides classifiers for common relational database management systems using a JDBC connection.  
  * **Connection:** AWS Glue Connection is the data catalog that holds the information needed to connect to a certain data storage.
  * **Data Store:** It is a repository for persistently storing our data. Examples include Amazon S3, buckets, and relational databases.
  * **Data Source:** It is a target data store that is used as an input to process or transform.
  * **Data Target:** It is a data store where the transformed data is written. 
  * **ETL Job:** It is a business logic required to perform the ETL work It is composed of a transformation script data sources and data targets. They can be initiated by triggers that can be scheduled or triggered by events. 
  * **Script:** It contains the code that extracts data from sources, transforms it, and loads it into the targets. 
  * **Transform:** We use the code logic to manipulate our data into different formats using the transform.
  * **Trigger:** It initiates an ETL job. We can define triggers based on a scheduled time or an event. 
  * **Notebook Server:** It is a web-based environment that we can use to run our PySpark statements, which is a Python dialect used for ETL programming. 
  * **Development Endpoint:** It is an environment where we can develop and test our AWS Glue ETL scripts.

<!-- Glue Data Catalog has connections, database, tables, settings, transformations.
You can create job which can use informations - metadata in Glue Data Catalog to create scripts.
And these scripts can be scheduled to move data from storage A (Data Source) to storage B (Data Target).
You can also access Glue Data Catalog thru AWS Management Console to do majority of work above, and you can also have command line as usual. -->