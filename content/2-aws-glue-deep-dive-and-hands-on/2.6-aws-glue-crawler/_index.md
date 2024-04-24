---
title : "AWS Glue Crawler"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 2.6. </b> "
---

#### AWS Glue Crawler
  * A program that connects to a data store (source or target).
  * Process thru a prioritized list of classifiers to determine the schema for your data; and then creates metadata tables in the AWS Glue Data Catalog.
  * **Data Discovery Tools:** Crawlers are an essential component of the AWS Glue service. They act like automated detectives, scanning various data sources to understand the structure and content of your data.
  * **Populating the Data Catalog:** Crawlers extract metadata (data about data) including:
    - Schema (column names, data types)
    - File formats (CSV, JSON, Parquet, etc.)
    - Partitions
    - Other relevant properties
  * **Updating Metadata:** Crawlers can be run on a schedule or on-demand to keep the AWS Glue Data Catalog up-to-date as your data evolves.

#### Key Benefits of AWS Glue Crawlers:
  * **Automation:**  Save time and effort by automating the process of discovering data structures and updating your data catalog. This removes manual work, especially for large datasets or evolving data sources.
  * **Metadata Centralization:**  Crawlers populate the AWS Glue Data Catalog, which serves as a central repository for metadata. This helps various AWS services (like Athena, Redshift Spectrum, or Glue ETL jobs) understand and work with your data seamlessly.
  * **Schema Inference:** Glue Crawlers can often infer the schema of your data automatically, reducing manual configuration needed when creating tables in the catalog.

### Types of Data Sources Supported:
  * **Amazon S3:** Crawl data stored in S3 Buckets in various formats.
  * **Relational Databases (RDS, DynamoDB, etc.):** Discover tables and their schemas contained within supported databases.
  * **Custom Classifiers:** You can extend a crawler's capabilities with custom classifiers to recognize new file formats or extract more specialized metadata.

#### Automation scan table by AWS Glue Crawler
  1. Go to [Glue console](https://ap-southeast-1.console.aws.amazon.com/glue/home?region=ap-southeast-1).
  2. Go to **Database**, then choose **customer_database** already created.
  3. Click **Add tables using crawler**
  ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-1.png)
  4. On **Set crawler properties** section:
     * Give the crawler a name: `customer_crawler`.
     * Click **Next**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-2.png)
  5. On **Choose data sources and classifiers** section:
     * Click **Add a data source**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-3.png)
     * Choose Data source: **S3**.
     * Choose S3 path: choose the path where the data file reside.
     * Click **Add an S3 data source**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-4.png)
     * Click **Next**.
  6. On **Configure security settings** section:
     * IAM role: choose IAM role already created in [2.1](../2.1-preparation)
     * Click **Next**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-5.png)
  7. On **Set output and scheduling** section:
     * Target database: `customer_database` (or you can choose any other database)
     * Crawler schedule: **On demaind**
     * Click **Next**.
     ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-6.png)
  8. Review again then click **Create crawler**.
  ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-7.png)
  9. Click **Run crawler** for execute crawler crawling table definition into Glue Data Catalog.
  ![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-crawler-8.png)
  9. Check result:
     * 

