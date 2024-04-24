---
title : "AWS Glue Tables"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 2.4. </b> "
---

#### AWS Glue Table
  * The **metadata definition** that represents your data. The data resides in its original store. This is just a representation of schema.
  * *For example:* You have a data file in S3, then you add this data into Glue Data Catalog. This data actually is still on S3, the data doesn't go anywhere. It only bring the schema infomation onto the Glue Data Catalog.
  * About metadata definition that will be scan onto Glue Data Catalog, may include:
    - **Name:** Table identifier
    - **Schema:** List of columns and their data types
    - **Location:** Where the data is physically stored (like an S3 bucket path)
    - **Partitions:** Subdivisions of tables for optimization
    - **Classifiers:** Define patterns to extract additional metadata

#### Table Partition in AWS
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/s3-partition.png)
  * **Partition in S3:**
    - Folders in S3 can act as a way to *represent* partitions for a corresponding table in your Glue Data Catalog. They provide a **physical organization** of your data files.
    - Each folder would typically correspond to a specific partition value (e.g., /year=2023/month=04/).
  * **Partition in Glue:**
    - These are **logical entities** within your Glue Data Catalog table definition.
    - They define a subset of the table's data based on the values of the partition columns (e.g., date, region).

Table Partition in AWS => The Glue Data Catalog connects the logical partitions to the physical folder structure on S3.

{{% notice note %}}
Data files themselves are stored within S3 folders that represent partitions.\
Columns in the Glue table: Partition columns are specific columns within your table schema that are used as the criteria to divide the data into partitions.
{{% /notice %}}

#### Manually Create Glue Table
  1. Go to [Glue console](https://ap-southeast-1.console.aws.amazon.com/glue/home?region=ap-southeast-1).
  2. Go to **Database**, then choose **customer_database** already created.
  3. Click **Create table** for manually create.
  ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table.png)
  4. On **Set table properties** section:
     * Give the table a name: `test_manual_customer_csv`.
     * Choose database: `customer_database`.
     * Description: `Manually create table onto Glue database`.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table-2.png)
     * Data store: **S3**.
     * Data location is specified in: **my account**.
     * Include path: choose the path where the data file reside.
     * Data format: **CSV**.
     * Delimeter: **Comma (,)**.
     * **Next**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table-3.png)
  5. On **Choose or define schema** section:
     * Choose **Define or upload schema** for manually define schema
     * Manually define column name, column type, click **Add**:
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table-4.png)
       - With **partition columns**:
         + Tick **Set as partition key?**.
         + Name: give a name like in data source (in this sample data, it's `client_created_date`).
         + Data type: give a datatype match with data source (in this sample data, it's `string`).
         ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table-5.png)
       - Other columns:
         + Name: give a name like in data source.
         + Data type: give a datatype match with data source.
         ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-table-6.png)
     * After add all columns, click **Next**.
     * Review again then click **Create**.    

As you can see, manually defining data columns for Glue Tables can be quite time-consuming. Is there a way to automate this repetitive task? \
=> Use AWS Glue Crawler!