# Summary

In this workshop, we will learn cataloging datasets using AWS Glue crawlers. We will interactively author ETL scripts in  SageMaker notebook on our local machine while being connected to an AWS Glue development endpoint. We will then deploy ETL scripts into production by turning your ETL script into managed AWS Glue jobs and add appropriate AWS Glue scheduling and triggering conditions. Finally, we will query these new datasets from Amazon Athena using AWS Glue Data Catalog.

Athena cost https://aws.amazon.com/athena/pricing/ ~ 6cents for 10 queries
AWS Glue Cost https://aws.amazon.com/glue/pricing/ ~ 50cents for one hour execution

> WARNING It is very important that you clean your workspace before you leave since Glue end points costs ~$50 per day. Please see [Cleanup](./CleanUp/README.md)

# Prerequisites

Cloud 9 set up is explained in Step1. This is the recommended set up. Alternatively, you might want to set up your local machine. This is a longer process and is explained [here](https://blog.programming-tools-meetup.cloud/dev-machine-setup/)

Rest of the meetup is organized based Cloud9 environment. Please choose your region as **us-east-1**

# Content

Today we will look into usage of Glue service using different functionality. AWS Glue is a fully managed ETL (extract, transform, and load) service that makes it simple and cost-effective to categorize your data, clean it, enrich it, and move it reliably between various data stores. AWS Glue consists of a central data repository known as the AWS Glue Data Catalog, an ETL engine that automatically generates Python code, and a flexible scheduler that handles dependency resolution, job monitoring, and retries. AWS Glue is serverless, so there's no infrastructure to set up or manage. Use the AWS Glue console to discover your data, transform it, and make it available for search and querying. You can also use the AWS Glue API operations to interface with AWS Glue.

## Step 1 Ingest Data

We will first set up the data from NYC taxi trips from Jan to March 2017 approximately 2M rows in 3 files and 2.5GB uncompressed data. We will also look at the glue catalog. You can start by going to [Step1](./Step1/README.md)

## Step 2 Clean Data

We will start querying our data using Athena. Athena is great way to do exploratory data analysis over unstructured data in S3. After initial investigation we will apply multiple transformations to data using Sagemaker Notebooks. You can start by going to [Step2](./Step2/README.md)

## Step 3 Productionize the ETL pipelne
We will take our Sagemaker notebook and build an automated ETL pipeline using Workflows. Workflow will kick in every day at 6:00am UTC and apply all transformations to the data. This section will finalize our workshop. You can start by going to [Step3](./Step3/README.md)

> WARNING It is very important that you clean your workspace before you leave since Glue end points costs ~$50 per day. Please see [Cleanup](./CleanUp/README.md)