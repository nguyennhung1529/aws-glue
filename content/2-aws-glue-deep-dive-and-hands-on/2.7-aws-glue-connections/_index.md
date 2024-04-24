---
title : "AWS Glue Connections"
date :  "`r Sys.Date()`" 
weight : 7 
chapter : false
pre : " <b> 2.7. </b> "
---
<!-- You can connect AWS Glue ETL jobs to a variety of data sources and destinations by using the pre-built connectors known as AWS Glue Connectors. These connectors offer a standardised method of interacting with various data sources and formats, making the process of extracting, transforming, and loading data easier. -->

#### What are AWS Glue Connections?
  * **Metadata for External Data Stores:** Glue Connections provide a way to **store and manage** the **connection details** required to access various **external data sources** from within AWS Glue.
  * **Simplified Management:** Instead of embedding connection strings directly in Crawler or ETL job code, you create reusable Glue Connection objects which store this information.

#### Key Components of a Glue Connection
  * **Connection Type:** Specifies the type of data store (e.g., JDBC for databases, S3, Network, or Marketplace for vendor-specific sources).
  * **Connection Properties:** The required information varies based on the type:
    - **Databases:** Hostname/IP, port, username, password, database name
    - **S3:** Bucket name, access keys (if not IAM role-based)
    - **Network:** VPC, Subnet, security groups (if connecting to sources within your VPC)
  * **Security:** Optionally define how to handle credentials (use IAM roles, store in Secrets Manager, etc.).

#### Benefits of AWS Glue Connections
  * **Centralized Management:** Update connection details in one place, impacting all jobs and crawlers using that connection.
  * **Security:** Avoid hardcoding sensitive credentials in your code. Glue Connections can integrate with AWS Secrets Manager for enhanced secret handling.
  * **Ease of Use:** Simplifies the configuration of crawlers and ETL jobs, as you can select pre-defined connections.
  * **Reusability:** A single connection can be used by multiple crawlers and jobs.

#### Supported Connection Types
  * JDBC: For connecting to relational databases like MySQL, PostgreSQL, Oracle, SQL Server, etc.
  * S3
  * Network: Enables access to data sources running inside your VPCs.
  * AWS Marketplace: Provides connectors for various vendor-specific sources and SaaS products.

<!-- #### How to Use Glue Connections
  * Create a Connection: In the AWS Glue console, go to "Connections" and create a new connection, providing the necessary details for your type of data source.
  * Crawlers: When configuring a crawler, choose the relevant connection instead of specifying access details directly within the crawler configuration.
  * ETL Jobs: Within your scripts, use functions from the AWS Glue library to access the data source using the Glue Connection name. -->

#### Hands-on Lab: Create a Glue connection refer to RDS database
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-create-connection-1.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-create-connection-2.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-create-connection-3.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-create-connection-4.png)
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-create-connection-5.png)