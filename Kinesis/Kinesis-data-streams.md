## Definition
Receives and temporarily retains large volumes of streaming data so applications can read and process it

eg. Collects thousands of transaction per second from an online store 

### Shards 
In between producers and consumers, there are shards which are partition of a Kinesis data stream that stores a sequence of data records and provides a certain amount of read and write capacity. 

In other words, shards are similar to lane on a highway and more lanes mean more traffic which in this case more throughput 


Data Streams has two Capacity Modes

1. On Demand 
- Use Case: Unpredictable workloads
- Management: Automatically scales
- Billing: volume of data ingested and retrived
- Capacity: writes 200 MiB per second, 200000 records per second, reads 400 MiB per second per consumer (2 consumer by default). Enhanced Fan-out (EFO) to add 20 more consumers

2. Provisioned
- Use Case: Predictable workloads
- Management: Customer manages shards
- Billing: Number of shards, data transfer
- Capacity: writes 1 MiB per second per shard, 1000 records per second per shard, reads 2 MiB per second per shard (max shard is 200)

### Partition Key
A partition key is a value associated with each record that Kinesis uses to determine which shard receives it

### Producers and Consumers
- Producer are the entities that produces the data that will be send through data streams 

- Consumers are the entities that receives and work on the data from the data streams

- Tools and technologies that help producers send their data to Kinesis
    - Amazon Kinesis Agent: Monitors files, such as application logs, and sends newly written data into Kinesis
    - AWS SDK: Allows your own application code to publish records using API operations such as PutRecord and PutRecords
    - AWS Direct Integration: other AWS services can send data into Kinesis through supported integrations 
    - Amazon Kinesis Producer Library (KPL): helps applications publish large numbers of records efficiently using batching and aggregation


- Tools and technologies that help consumers receive the data from Kinesis
    - third-party tools: external framework and connectors, such as Apache Flink or Kafka Connect, can be configured to read and process Kinesis records 
    - Amazon Data Firehose: reads Kinesis records and automatically delivers them to destinations such as S3 or Redshift 
    - AWS SDK: lets your application retrieve records using APIs such as GetRecords 
    - Kinesis Client Library (KCL) helps build consumers the efficiently read and process records across multiple shards

### Sequence number
A sequence number is a unique identifier assigned by Kinesis to each data record within a shard 

Two main reason for why we need sequence numbers:
1. Maintaining record order
2. Tracking the consumer progress 

### Retention period
This is how long data will remain in the stream until it is released (deleted)

- Data persist for 24 hours (default)
- Data can be changed to persist for 8760 hours (365 days)