# Clean up your account

Once you are done with the lab, follow the instructions below to clean-up your account. First, delete manually-created AWS Glue resources.
- Navigate to the AWS Glue console
- Go to **Databases** then select **nyctaxi**. Click Action, then Delete database. Confirm deletion.
- Go to **Crawlers** then select each **nyctaxi-optimized-crawler**, **nyctaxi-raw-crawler**. Click Action, then Delete crawler. Confirm deletion.
- Go to **Workflows** and select delete workflow **NYC production workflow**
- Go to **Jobs**, then select **nyctaxi-create-optimized-dataset**. Click Action, then Delete. Confirm deletion.
- Go to **Triggers**, then select **nyctaxi-raw-crawler-SUCCESS**, **6amScheludedTrigger**, and **nyctaxi-create-optimized-dataset-job-SUCCESS**. Click Action, then Delete. Confirm deletion.
- Go to **Notebooks**, then select **aws-glue-nyctaxi-notebook**. Click Action, then Stop. Wait until notebook status changes to Stopped. Click Action again, then Delete.
- Finally go to S3 and delete buckets
  - **melbournecloudtoolsmeetup.xxxx** bucket
  - **aws-athena-query-results-xxx**
  - **aws-glue-scripts-xxx**
  - **aws-glue-temporary-xxxx**

Finally, delete the workshop's AWS CloudFormation stack to clean-up remaining resources.
- Navigate to the AWS CloudFormation console
- Select the workshop's stack **CloudToolsMeetup-JAN-Crawler**, **CloudToolsMeetup-JAN-Glue**, and **CloudToolsMeetup-JAN-Athena** in this order. Click Actions, then Delete stack. Confirm deletion.
- Stack status will change to DELETE_IN_PROGRESS. The stack should take less than a minute to be deleted.
- Delete Cloud9 instance from the Web console.

You're done cleaning-up your account!

>WARNING: After deleting the stacks make sure Glue ETL **Dev endpoints** will have no endpoints since keeping it up will cost you ~$50 daily.