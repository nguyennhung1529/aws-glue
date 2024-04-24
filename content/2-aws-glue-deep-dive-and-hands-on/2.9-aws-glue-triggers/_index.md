---
title : "AWS Glue Triggers"
date :  "`r Sys.Date()`" 
weight : 9 
chapter : false
pre : " <b> 2.9. </b> "
---

#### AWS Glue Triggers
  * Initiates an ETL job.
  * Can be defined based on a scheduled time or an event.

#### Types of Glue Triggers:
  1. **Scheduled Triggers:**
     * **Cron Expressions:** Run Crawlers or Jobs on a recurring schedule using Cron or simplified rate expression (e.g., run every hour, every Monday at 8 am, etc.).
     * **Benefits:** Regularly update your Data Catalog with fresh data or run ETL jobs on a predictable timetable.
  2. **On-demand Triggers:**
     * Manual Execution: Start a Glue Crawler or ETL Job manually through the console or API.
     * **Benefits:** Useful for one-time execution, testing, or backfilling data.
  3. **Event-based Triggers:**
     * **Conditional Start:** Launch a Crawler or Job in response to specific events in other AWS services. \
       *Examples:*
       - An S3 object is created or modified in a specific bucket.
       - An AWS Lambda Function execution succeeds.
       - A previous Job or Crawler completes its run.
     * **Benefits:** Create dynamic, reactive data processing pipelines.

<!-- #### Benefits of Using Glue Triggers
   * Automated Data Catalog Updates: Keep your Glue Data Catalog up-to-date with the latest data without manual intervention.
   * Scheduled ETL Pipelines: Define regular data processing workflows for cleaning, transforming, and loading data.
   * Event-driven Workflows: React to changes in your data sources or other AWS services, making your data pipelines more responsive.
   * Enhanced Operational Efficiency: Reduce manual tasks and streamline your data management processes.

#### Use Cases
  * Regular Data Ingestion: Schedule a Crawler to discover new data in S3 buckets and update the Data Catalog on a daily or hourly basis.
  * Incremental ETL: Process files as they arrive in S3 buckets, transforming and loading them into target systems.
  * Dependent Pipelines: Chain together ETL jobs, where completion of one job triggers the next step.
  * Backfilling and Re-processing: Use on-demand triggers to re-run jobs for historical data or error correction. -->

#### Hands-on Lab
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-1.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-2.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-3.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-4.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-5.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-6.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-7.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-8.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-9.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-10.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-11.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-12.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-trigger-13.png)