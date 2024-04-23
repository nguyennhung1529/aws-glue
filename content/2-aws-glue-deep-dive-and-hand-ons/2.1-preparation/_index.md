---
title : "Preparation"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1. </b> "
---
There are a few steps you’ll need to take to prepare your AWS account and the tools and files you need before starting the AWS Glue hand-on labs:

  1. **AWS Account** – for hand-ons lab
  2. **S3 Bucket** – for storing data source, data target, and script, ect
  3. **IAM Role for AWS Glue**

Let's login to AWS Console, then following below step:
#### Create S3 Bucket
In this step, we will create new S3 bucket with folder and sub-folders for storing data source, data target, script job, etc. But first of all, we will just create S3 bucket.
  1. Go to [S3 console](https://ap-southeast-1.console.aws.amazon.com/s3/buckets?region=ap-southeast-1)
  2. Go to **Bucket**, then click **Create bucket**
  ![S3](/images/2-aws-glue-deep-dive-and-hand-ons/s3-bucket-create.png)
  3. Give the bucket a name: `aws-glue-labs-bucket`
  4. Click **Create bucket**.
  ![S3](/images/2-aws-glue-deep-dive-and-hand-ons/s3-bucket-create-2.png)

Next, we will create folder for storing data source. We will:
  * Create folder `source/` for storing source/raw data.
  * Create sub-folder `source/customer_database`
  * Create sub-folder `source/customer_database/customers_info_csv`
  * Create sub-folder `source/customer_database/customers_info_csv/client_created_date=20240423`
  * Upload data into `client_created_date=20240423`

  1. Go to **aws-glue-labs-bucket** bucket, then click **Create folder**
  ![S3](/images/2-aws-glue-deep-dive-and-hand-ons/s3-bucket-create-folder.png)
  2. Give the folder a name: `source`
  3. Click **Create folder**.
  ![S3](/images/2-aws-glue-deep-dive-and-hand-ons/s3-bucket-create-folder-2.png)

Repeat the steps above, and you will have:
  * sub-folder `source/customer_database`
  * sub-folder `source/customer_database/customers_info_csv`
  * sub-folder `source/customer_database/customers_info_csv/client_created_date=20240423`

To upload data into folder `client_created_date=20240423`:
  1. Download data get from link github
  * Upload data into `client_created_date=20240423`


#### Create IAM Role