---
title : "What is AWS Glue?"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 1.1. </b> "
---

![AWSGlue](/images/1-overview-aws-glue/aws-glue-icon.png)

  * AWS Glue is a **fully managed ETL service**
  * Consists of a Central Metadata Repository - Glue Data Catalog
  * Spark ETL Engine (completely serverless)
  * Flexible scheduler: Custom ETL jobs on trigger-driven, on a schedule, or on-demand

<!-- Glue Data Catalog stands in the middle, it has connections, tables, settings, transformations.
You can create job which can use informations - metadata in Glue Data Catalog to create scripts.
And these scripts can be scheduled to move data from storage A to storage B.
You can also access Glue Data Catalog thru AWS Management Console to do majority of work above, but you can also have command line as usual -->