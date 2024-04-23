---
title : "AWS Glue Pricing"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 1.4. </b> "
---

{{% notice note %}}
AWS Glue follows a pay-as-you-go pricing model based on the resources consumed, including the execution time of ETL jobs and storage of metadata in the Glue Data Catalog. Pricing specifics depend on the volume of data processed and the duration of job execution.
{{% /notice %}}

  * **AWS Glue Crawlers and ETL jobs:** pay an hourly rate, billed by the second, depend on the volume of data processed and the duration of job execution.
  * **AWS Glue Data Catalog:** pay a simplified monthly fee for storing and accessing the metadata. The first million objects stored are free, and the first million accesses are free. 
  * **AWS Glue Development Endpoint:** pay an hourly rate, billed per second. 
  * **AWS Glue DataBrew:** the interactive sessions are billed per session, and DataBrew jobs are billed per minute. 
  * **AWS Glue Schema Registry:** no additional charge.
  ![AWSGluePricing](/images/1-overview-aws-glue/pricing-aws-glue-etl.png)

*For more information: [glue-pricing](https://aws.amazon.com/glue/pricing/)*