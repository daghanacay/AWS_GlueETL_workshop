# Summary

In this workshop, we will learn cataloging datasets using AWS Glue crawlers. We will interactively author ETL scripts in  SageMaker notebook on our local machine while being connected to an AWS Glue development endpoint. We will then deploy ETL scripts into production by turning your ETL script into managed AWS Glue jobs and add appropriate AWS Glue scheduling and triggering conditions. Finally, we will query these new datasets from Amazon Athena using AWS Glue Data Catalog.

Athena cost https://aws.amazon.com/athena/pricing/ ~ 6cents for 10 queries
AWS Glue Cost https://aws.amazon.com/glue/pricing/ ~ 50cents for one hour execution

# Prerequisites

Cloud 9 set up: Please follow the instructions [here](https://docs.aws.amazon.com/cloud9/latest/user-guide/tutorial-create-environment.html) to set up your cloud 9 instance. This is the recommended set up. Alternatively, you might want to set up your local machine. This is a longer process and is explained [here](https://blog.programming-tools-meetup.cloud/dev-machine-setup/)

Rest of the meetup is organized based Cloud9 environment. Please choose your region as **us-east-1**



