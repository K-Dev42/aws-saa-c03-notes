AWS SQS First-In-First-Out (FIFO) guarantee the order of messages when being consumed 

- Limited to 300 transaction per second (TPS)
- Messages have a unique duplication ID to ensure there are no duplicate messages in the queue. Since there are no duplicates FIFO ensures exactly one processing
- Messages are ordered based on Message Group Id
- To ensure order is preserved each Producer should use their own unique Message Group Id
- To request (pull) messages, your Consumer has to specify a Message Group Id 
- it's possible to read upto 10 messages at a time
- SQS FIFO manages data partitions across multiple AZs, but it's all managed for you by AWS 

High Throughput can be enabled on SQS FIFO queue to allows for 3000 messages per second with batching (10X greater than SQS FIFO queue without High Throughput)