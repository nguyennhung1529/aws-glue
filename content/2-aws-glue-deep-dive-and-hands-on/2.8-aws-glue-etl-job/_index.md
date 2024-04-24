---
title : "AWS Glue ETL Job"
date :  "`r Sys.Date()`" 
weight : 8 
chapter : false
pre : " <b> 2.8. </b> "
---
#### What are AWS Glue ETL Jobs?
  * **Managed ETL Service:** Glue ETL jobs provide a way to extract, transform, and load (ETL) your data within AWS. These are serverless units of work designed to move and process data between different data stores or prepare it for analysis.
  ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/glue-job-icon.png)
  * **Code-Based or Visual:** You can create Glue ETL jobs in two ways:
    - **Visual Editor:** Use the drag-and-drop interface to build ETL workflows with less code for simpler scenarios.
    - **Python or Scala Scripts:** Write code using the Glue libraries (**pyspark** or **spark**) for complex transformations.
      + Create job with **Glue Notebooks** (suitable for testing / development environment):
        + Data exploration and analysis
        + Prototyping ETL code before deploying as regular jobs
        + One-off tasks with an interactive element
      + Create job with **Glue Script editor** (suitable for production environment):
        + Regular ETL processes needing automation and scheduling
        + Production data pipelines where reliability is crucial

{{% notice note %}}
You can convert your notebook code into an ETL job, making the transition from development to production easier.
{{% /notice %}}

#### Key Components of Glue ETL Jobs
  * **Data Source:** Defines where the job should read data from. This can be S3 buckets, databases (RDS, Redshift, etc.), or other Glue Data Catalog tables.
  * **Transformations:** The core logic of your ETL job.
  * **Built-in Transforms:** Glue provides numerous pre-built transformations for filtering, joining, cleaning, and aggregating data.
  * **Custom Code:** Utilize Python (PySpark) or Scala (Spark) for complex logic.
  * **Data Target:** Where the processed/transformed data should be loaded. This could be another S3 location, a database, or another Glue table.
  * **Triggers:** Determine how a job is executed:
    - **On-Demand:** Manually run the job.
    - **Scheduled:** Run the job on a schedule (e.g., daily, weekly).
    - **Event-Based:** Run the job in response to events (e.g., a new file arriving in S3).

#### Benefits of AWS Glue ETL Jobs
  * **Serverless:** No need to provision or manage servers. Glue handles the resource allocation and scaling of your jobs.
  * **Data Catalog Integration:** Jobs utilize the metadata in the Glue Data Catalog, making it easy to find and work with your data sources and targets.
  * **Flexibility:** Use the visual editor and built-in transforms for simple ETL or write code for advanced customization.
  * **Development and Debugging:** AWS Glue Studio provides an integrated environment for developing, testing, and debugging your ETL jobs.

#### Hands-on labs
  2.8.1. [Create Job with Visual Editor](2.8.1-create-job-with-visual-editor/) \
  2.8.2. [Create Job with Glue Notebooks](2.8.2-create-job-with-glue-notebooks/) \
  2.8.3. [Create Job with Glue Script editor](2.8.3-create-job-with-glue-script-editor/)