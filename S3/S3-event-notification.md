## Definition
S3 Event Notification allows your bucket to notify other AWS services about S3 event data. Or in other words, S3 event Notification makes application integration very easy for S3 

Notification events
    - New object created events
    - Object removal events 
    - Restore object events 
    - Reduced Redundancy Storage (RRS) object lost events 
    - Replication events 
    - S3 Lifecycle expiration events 
    - S3 Lifecycle transition events 
    - S3 Intellignet-Tiering automatic archival events 
    - Object tagging event
    - Object ACL PUT events

Possible Destination to other AWS services
    - Amazon Simple Notification Service (SNS) topics
    - Amazon Simple Queue Service (SQS) queues
    - AWS Lambda function
    - Amazon EventBridge 

> Amazon S3 event notification are designed to be delivered at least once. Notification are delivered in seconds but can sometimes take a minute or longer. This feature of S3 is regarded to be super useful by professional. 