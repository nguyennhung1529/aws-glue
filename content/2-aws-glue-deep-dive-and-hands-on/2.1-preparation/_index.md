---
title : "Preparation"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1. </b> "
---
There are a few steps you’ll need to take to prepare your AWS account and the tools and files you need before starting the AWS Glue hand-on labs:

  1. **AWS Account** – for hands-on lab
  2. **S3 Bucket** – for storing data source, data target, and script, ect
  3. **IAM Role for AWS Glue**

Let's login to AWS Console, then following below step:
#### Create S3 Bucket
In this step, we will create new S3 bucket with folder and sub-folders for storing data source, data target, script job, etc. But first of all, we will just create S3 bucket.
  1. Go to [S3 console](https://ap-southeast-1.console.aws.amazon.com/s3/buckets?region=ap-southeast-1)
  2. Go to **Bucket**, then click **Create bucket**
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/s3-bucket-create.png)
  3. Give the bucket a name: `aws-glue-labs-bucket`
  4. Click **Create bucket**.
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/s3-bucket-create-2.png)

Next, we will create folder for storing data source. We will:
  * Create folder `raw_data/` for storing source/raw data.
  * Create sub-folder `raw_data/customer_database`
  * Create sub-folder `raw_data/customer_database/customers_csv`
  * Create sub-folder `raw_data/customer_database/customers_csv/client_created_date=20240423`
  * Upload data into `client_created_date=20240423`

  1. Go to **aws-glue-labs-bucket** bucket, then click **Create folder**
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/s3-bucket-create-folder.png)
  2. Give the folder a name: `raw_data`
  3. Click **Create folder**.
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/s3-bucket-create-folder-2.png)

Repeat the steps above, and you will have:
  * sub-folder `raw_data/customer_database`
  * sub-folder `raw_data/customer_database/customers_csv`
  * sub-folder `raw_data/customer_database/customers_csv/client_created_date=20240423`

To upload data into folder `client_created_date=20240423`:
  1. Download data get from link [github](https://github.com/nguyennhung1529/aws-glue)
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/customer-data-source.png)
  2. Upload data file into `client_created_date=20240423`, then click **Upload**
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/customer-data-source-upload.png)

As you can see, data file is uploaded successfully into S3. 
Next, we will create IAM Role for AWS Glue
#### Create IAM Role
  1. Go to [IAM console](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/home)
  2. Go to **Role**, click **Create role**
  ![S3](/images/2-aws-glue-deep-dive-and-hands-on/IAM-role-create.png)
  3. On **Select trusted entity** section:
     * Trusted entity type: **AWS Service**
     * Service or use case: **Glue**
     * Click **Next**
     ![S3](/images/2-aws-glue-deep-dive-and-hands-on/IAM-role-create-2.png)
  4. On **Add permissions** section:
     * Select `AWSGlueServiceRole` and `S3FullAccess` from **Attach Permissions Policies**
     * Click **Next**.
  5. On **Name, review, and create** section, 
     * Set Role name**: `glue-full-access`
     * Review then click **Create role**.
     ![S3](/images/2-aws-glue-deep-dive-and-hands-on/IAM-role-create-3.png)

In the next section, we'll hands-on AWS Glue on the console.