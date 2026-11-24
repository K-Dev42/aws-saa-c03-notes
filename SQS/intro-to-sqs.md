## Definition
What is a Messaging System?
Used to provide asynchronous communication and decouple processes via messages / events

From a sender and receiver (producer and consumer)

What is a queueing System?
A queueing system is a messaging system that generally will delete messages once they are consumed. Simple communication. **Not Real-time**. Have to pull. Not reactive. 


Simple Queueing Service (SQS)
Fully managed queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications


Use Case: You need to queue up transaction emails to be sent eg. Signup, Reset Password 

SQS Queue types:
1. Standard: allows you to process a nearly unlimited amount of messages, but messages are out of order 

2. FIFO: allows you to process a certain amount of message, but guarantee order of message and no duplicate messages

Message Size:
The size of a message can be between 1 byte and 256 KiB
For larger messages you need to use a library 

Message Retention is how long SQS will hold onto a message in the queue before dropping it from the queue (deleting it)
- Message retention by default is 4 days
- Message retention can be adjusted from a minimum of 60 seconds to a max of a4 days

Queue Encryption 
SQS queue can be encrypted using Amazon managed Server-Side-Encryption (SSE) or using KMS 