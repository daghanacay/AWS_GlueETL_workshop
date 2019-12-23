# Query Raw Data with Amazon Athena

You can directly go to [Athena Console](https://console.aws.amazon.com/athena/home?force&region=us-east-1#query) and start querying your NYC data using Glue Catalog created previously. Amazon Athena is a serverless interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. It integrates with the AWS Glue data catalog and takes advantage of the metadata registered by AWS Glue crawlers.

However, we would like to generate a pre-canned queries for you so you can modify them. In order to get the Athena queries run the following on Cloud9 environment. But move to Step2 folder first, ```cd ../Step2``` and run

```aws cloudformation deploy --template-file setup_athena.yaml --stack-name CloudToolsMeetup-JAN-Athena --capabilities CAPABILITY_NAMED_IAM```

After the stack creation is finished. Navigate to [Athena Console](https://console.aws.amazon.com/athena/home?force&region=us-east-1#query) console

- Ensure database nyctaxi is selected, and the four tables are listed: yellow, paymenttype, ratecode, and taxizone.
- Click on the tab Saved Queries
- In the search field, type nyctaxi:raw
- Click on the **sample_report_qry** query to open in Athena query editor Note: After opening the query, review the comment before the SQL statement.
- Click Run query
- Note query run time and data scanned. Copy and paste it into an open text file for later comparison.
- Repeat above steps for query **sample_agg_qry**