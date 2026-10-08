AWS offers a range of S3 storage classes that *trade* **Retrieval Time**, **Accessibility**, and **Durability** for cheaper storage. 

### S3 standard (default)
Fast, available, and durable

Characteristics of the default storage class
- **High durability**: 11 9's of durability
- **High availability**: 4 9's of availability
- **Data redundancy**: data stored in 3 or more availability zones
- **Retrieval time**: within milliseconds (low latency) 
- **High throughput**: optimized for data that is frequently accessed and/or requires real-time access
- **Scalability**: easily scales to storage size and number of requests
- **Use cases**: ideal for a wide range of use cases like content distribution, big data analytics, and mobile and gaming applicaitions, where frequent access is required. 
- **Pricing**: storage per GB, per requests, not retrieval fee, no minimum storage duration charge


### S3 intelligent tiering
Uses ML to analyze object usage and determine storage class. Extra fee to analyze


### S3 express one-zone
Single-digit ms performance, special bucket type, one AZ, 50% less than standard cost

Characteristics of the express one zone class
- Has the lowest latency compared to all of the other storage class
- Data access speeds up to **10x faster** than S3 standard
- Request costs **50% lower** than that of S3 standard 
- Data is stored in a user selected single availability zone 
- Data is stored in a new bucket type: **an Amazon S3 directory bucket** (limit of 10 per account)
- **Pricing**: applies a flat per request charge for request sizes upto 512 KB


### S3 standard-IA (infrequent access)
Fast, cheaper if you access less than once a month. It has extra fee to retrieve. 50% less than standard (reduced availability)

Characteristics of the standard-IA storage class
- **High durability**: 11 9's of durability
- **High availability**: 3 9's of availability
- **Data redundancy**: data stored in 3 or more availability zones
- **Cost-Effective Storage**: costs 50% less from standard. As long as you don't access a file more than once a month
- **Retrieval time**: within milliseconds (low latency)
- **High throughput**: optimized for rapid access, although the data is accessed less frequently compared to S3 standard
- **Use cases**: Ideal for data that is accessed less frequently but requires quick access when needed, such as disaster recovery, backups, or long-term data stores where data is not frequently accessed 
- **Pricing**: storage per GB, per requests, has a retrieval fee, has a minimum storage duration charge of 30 days


### S3 one-zone-IA 
Fast objects only exist in one AZ. Cheaper than Standard IA by 20% less 
(Reduce durability) data could get destroyed. Extra fee to retrieve


### S3 Glacier storage service
**S3 Glacier Instant Retrieval** for long-term cold storage. Get data instantly
**S3 Glacier Flexible Retrieval** takes minutes to hours to get data (Standard, Expidiated, Bulk Retrieval)
**S3 Glacier Deep Archive** the lowest cost storage class. Data retrieval time is 12 hours 

> S3 outpost has its own storage class.
> There is another storage class but it is just a legacy class with no real cost benefit and that is S3 reduced redundancy storage (RRS)
> You can change storage class anytime you want and you can do that via aws cli. the syntax are as follow --> aws s3 cp hello.txt s3://examplebucketname --storage-class STANDARD_IA