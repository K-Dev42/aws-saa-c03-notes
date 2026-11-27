## Definition
Amazon Data Firehose allows for simple transformation and delivery of data 

For this service, we do not utilize shards

- You choose one consumer from a predefined list
- Data immediately disappears once it's consumed 
- You can convert incoming data to a few other file formats and compress and secure data 
- You pay only for data that is ingested 

### Producers
Data Firehose allows easily configure a source or sources of data often with minimal or no programming skills 

### Consumers
Data Firehose can send to specific AWS services, third party services or an HTTP endpoint

AWS Services Destinations
- Amazon S3
- Amazon Redshift
- Amazon OpenSreach Service
- Amazon OpenSearch Serverless 

Custom Destinations
- HTTP endpoint 

Third-party destinations
- Splunk
...

> Each destination has different destination configuration options, often third-party apps need an API key from the provider 

### Data transformation
Before data is sent to a destination it can be transformed with AWS Lambda 

When enabled Firehose will buffer incoming data 
- You can change the buffer size: 0.2 to 3MB 
- You can change the buffer interval 0-900 seconds 

> There is a payload size limit of 6MB for both the Lambda request and the response 

When transforming data you need to ensure you return a json payload with the following:
- RecordID: the original record id passed from Firehose
- result: 
    - OK
    - Dropped
    - Processing failed
- Data:
    - The transformed data base64 encoded 

### Dynamic Partitioning
it is a feature that automatically organizes streaming data into different groups before storing it in Amazon S3 

To select the key and values for partiitoning you have two ways:
- Inline Partitioning: you provide a JQ expression to parse JSON
- Lambda function: you have a lambda parse the data and return the key and value

> Once enabled you cannot turn off Dynamic Partitioning on a Firehose stream 