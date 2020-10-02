# Data Pipeline  Load Tab Separated Files in S3 to Redshift 


## Running this sample
The pipeline requires the following user input point:

1. The S3 folder where the input TSV files are located. 
2. Redshift connection info along with the target table name.
3. Redshift Cluster security group id(s).



## Run this sample pipeline using the AWS CLI

```sh 
  $> aws datapipeline create-pipeline --name copy_tsv_to_redshift_pipeline --unique-id copy_tsv_to_redshift_pipeline
```

You receive a pipelineId like this. 
```sh
  #   -----------------------------------------
  #   |             CreatePipeline             |
  #   +-------------+--------------------------+
  #   |  pipelineId |  <Your Pipeline ID>      |
  #   +-------------+--------------------------+
```

```sh
  $> aws datapipeline put-pipeline-definition --pipeline-definition file://pipeline.json --parameter-values
     myInputTsvFilesS3Loc=<s3://tsv-files-insert-loc> myRedshiftJdbcConnectStr=<jdbc:postgresql://endpoint:port/database?tcpKeepAlive=true> myRedshiftUsername=<user> myRedshiftPassword=<your-red-password>
     myRedshiftTableName=<target-redshift-tablename> myRedshiftSecurityGrpIds=<sg-blah> --pipeline-id <Your Pipeline ID> 
```

You receive a validation messages like this
```sh
  #   ----------------------- 
  #   |PutPipelineDefinition|
  #   +-----------+---------+
  #   |  errored  |  False  |
  #   +-----------+---------+
```

Now activate the pipeline
```sh
  $> aws datapipeline activate-pipeline --pipeline-id <Your Pipeline ID>
```

Check the status of your pipeline 
```sh
  >$ aws datapipeline list-runs --pipeline-id <Your Pipeline ID>
```

You will receive status information on the pipeline. 


