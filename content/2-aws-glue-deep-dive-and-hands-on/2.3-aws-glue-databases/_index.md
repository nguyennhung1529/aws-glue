---
title : "AWS Glue Databases"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 2.3. </b> "
---

**AWS Glue Databases** - A set of associated Data Catalog table definitions organized into logical group.

{{% notice note %}}
AWS Glue Database is just a **name convention** to **logically organize tables** into a group. It's **not physically moving** tables or data to anywhere. Tables and data are still reside in it orgirinal locations
{{% /notice %}}

#### Create AWS Glue database
  1. Go to [Glue console](https://ap-southeast-1.console.aws.amazon.com/glue/home?region=ap-southeast-1).
  2. Go to **Database**, then click **Add database**.
  3. Provide a name, description (option), and location refer database (option):
     * **Name:** `customer_database`
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-database.png)
{{% notice info %}}
If you plan to access the database from **Amazon Athena**, then provide a name with only alphanumeric and underscore '_' characters. For more information, see [Athena names](https://docs.aws.amazon.com/athena/latest/ug/tables-databases-columns-names.html#ate-table-database-and-column-names-allow-only-underscore-special-characters).
{{% /notice %}}

     * **Description:** `this is a customer database`
     * **Location:** S3 database folder path
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-database-2.png)
{{% notice note %}}
In fact, you may not need to create physical database folders in S3, and you can just leave blank the location option in Glue Database. That's okay. However, it will be easier to manage when you create a well-structured physical folder hierarchy in S3 and then reflecting that structure with corresponding databases and tables in AWS Glue
{{% /notice %}}