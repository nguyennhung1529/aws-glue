---
title : "AWS Glue Data Catalog"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2. </b> "
---

#### AWS Glue Data Catalog - Persistent metadata store
  * It a managed service that lets you store, annotate, and share **metadata** which can be used to query and transform data.
  * One AWS Glue Data Catalog per Region.
  * IAM policy control access.
  * Can be used for data governance.
![Glue](/images/2-aws-glue-deep-dive-and-hands-on/aws-glue-console.png)

#### Key Metadata Components in AWS Glue
  * **Databases:** Logical groupings of tables.
  * **Tables:** Contain the actual data and these have:
    - **Name:** Table identifier
    - **Schema:** List of columns and their data types
    - **Location:** Where the data is physically stored (like an S3 bucket path)
    - **Partitions:** Subdivisions of tables for optimization
    - **Classifiers:** Define patterns to extract additional metadata

<!-- {{% notice note %}}
AWS Glue Data Catalog - **A centralised metadata repository** that houses information about your data from multiple data sources. It offers a single interface for finding, comprehending, and managing your data assets. It is used by an AWS Glue ETL job during execution to comprehend data properties and guarantee proper transformation.
{{% /notice %}} -->

---------------------------------------------------
{{% notice info %}}
  **So, what is Metadata?** \
  Simply put, **metadata** is information that describes other data. It's like a label or summary attached to a file, object, or dataset. \
  Metadata doesn't describe the content itself, but rather the characteristics of the data. \
  \
  **Examples:** \
  Document: Title, author, creation date, file size, keywords, word count \
  Image: Camera model, capture date and time, location (GPS), image dimensions, resolution, color information \
  Email: Sender, recipient, subject line, date and time sent, attachment details \
  Website: Keywords, description, author, last updated, page language
{{% /notice %}}

<!-- **Types of Metadata:**
  * **Descriptive Metadata:** Aids in discovery and identification. Examples include titles, authors, subjects, and keywords.
  * **Structural Metadata:** Describes how data is organized and put together. Examples include file formats, internal structure, relationships between data elements.
  * **Administrative Metadata:** Helps manage resources. Examples include creation/modification dates, access rights, and preservation information.

**Why is Metadata Important?**
  * **Organization:** Metadata helps categorize and organize vast amounts of data, making it easily searchable.
  * **Discovery:** It makes finding specific data or resources quick and efficient.
  * **Understanding:** Provides context about the data – its origin, purpose, structure, etc.
  * **Management:** Facilitates data management processes like preservation, access rights, and versioning.
  * **Interoperability:** Allows different systems to exchange and understand data.
  * **Trustworthiness:** Provides evidence of data's reliability and history. -->
<!-- 
**AWS Glue Data Catalog**
  * **Central Repository:** The AWS Glue Data Catalog acts as the **core metadata storage** for your data assets within AWS. It stores **information about databases, tables, schemas, and more**.
  * **Organization and Accessibility:** It **organizes metadata** in a **structured** way, making it **easy** for Glue jobs, crawlers, users, and other AWS services to **find and understand** relevant data.

**How Glue Uses Metadata**
  * **ETL Jobs:**
    - **Schema Inference:** When you write Glue ETL jobs, they analyze source data and use metadata to understand data structures for transformation and loading.
    - **Target Definition:** Metadata defines where data will be loaded (e.g., an S3 bucket or a database), aiding in the output process. 
  * **Data Discovery with Crawlers:**
    - **Crawlers:** These tools scan data sources (databases, S3, etc.) and automatically discover schemas and key properties.
    - Populating the Data Catalog: Crawlers extract metadata and update the AWS Glue Data Catalog, keeping it up-to-date.
    - **Querying:** Once metadata is in the catalog, users can search and query it to find datasets or tables they need. 
  * **Metadata Enhancements:**
    - **Classifiers:** You can add custom classifiers to crawlers to extract more specific metadata (like identifying PII columns or data formats).

**Key Metadata Components in AWS Glue**
  * **Databases:** Logical groupings of tables.
  * **Tables:** Contain the actual data and these have:
    - **Name:** Table identifier
    - **Schema:** List of columns and their data types
    - **Location:** Where the data is physically stored (like an S3 bucket path)
    - **Partitions:** Subdivisions of tables for optimization
    - **Classifiers:** Define patterns to extract additional metadata

**Benefits of Metadata in AWS Glue**
  * **Simplified ETL Development:** Leverages metadata to automate job creation.
  * **Seamless Data Understanding:** Helps users explore available data and how it's structured.
  * **Automated Metadata Management:** Crawlers keep the Data Catalog updated.
  * **Efficient Data Preparation:** Metadata informs optimal data transformation and loading. -->
