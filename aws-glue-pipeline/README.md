# AWS Glue ETL Code

### Examples
 - [Join and Relationalize Data in S3](examples/join_and_relationalize.md)

   This sample ETL script shows you how to use AWS Glue to load, transform,
   and rewrite data in AWS S3 so that it can easily and efficiently be queried
   and analyzed.

 - [Clean and Process](examples/data_cleaning_and_lambda.md)

   This sample ETL script shows you how to take advantage of both Spark and
   AWS Glue features to clean and transform data for efficient analysis.

 - [The `resolveChoice` Method](examples/resolve_choice.md)

   This sample explores all four of the ways you can resolve choice types
   in a dataset using DynamicFrame's `resolveChoice` method.

 - [Converting character encoding](examples/converting_char_encoding.md)
 
   This sample ETL script shows you how to use AWS Glue job to convert character encoding.

### Utilities

 - [Hive metastore migration](utilities/Hive_metastore_migration/README.md)

   This utility can help you migrate your Hive metastore to the
   AWS Glue Data Catalog.

 - [Crawler undo and redo](utilities/Crawler_undo_redo/README.md)

   These scripts can undo or redo the results of a crawl under
   some circumstances.

 - [sagemaker_notebook_automation](utilities/sagemaker_notebook_automation/README.md)
 
   An AWS CloudFormation template to launch the SageMaker Notebook with Glue Development Endpoint.
   
 - [Spark UI](utilities/Spark_UI/README.md)

   You can use this Dockerfile to run Spark history server in your container.
   See details: [Launching the Spark History Server and Viewing the Spark UI Using Docker ](https://docs.aws.amazon.com/glue/latest/dg/monitor-spark-ui-history.html#monitor-spark-ui-history-local)

 - [use only IAM access controls](utilities/use_only_IAM_access_controls/README.md)
 
   AWS Lake Formation applies its own permission model when you access data in Amazon S3 and metadata in AWS Glue Data Catalog through use of Amazon EMR, Amazon Athena and so on. 
   If you currently use Lake Formation and instead would like to use only IAM Access controls, this tool enables you to achieve it.
