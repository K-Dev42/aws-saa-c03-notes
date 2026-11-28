## Definition
AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account 

AWS CloudTrail is used to monitor API calls and actions made on an AWS account 

Easily identify which users and accounts made the call to AWS eg.
- Where: source IP address
- When: EventTime
- Who: User, UserAgent 
- What: Region, Resource, Action

CloudTrail is already logging by default and will collect logs for last 90 days via event history. If you need more than 90 days you need to create a Trail. 

Trails: are output to S3 and do not have GUI like event history. To analyze a Trail you'd have to use Amazon Athena 

### Types of events that CloudTrail record
1. Management events: operations that manage AWS resources eg. Creating an EC2 instance

2. Data events: operations involving data within supported resources eg. reading an S3 object

3. Insight events: unusual patterns in API activity eg. an exptected spike in API calls 

### Distinction between similar sounding services 
- CloudTrail exlains to us who performed an AWS action, and when?

- CloudWatch: how are my applications and resources performing? 

- AWS config: how my AWS resources are configured, and how have those configurations changed? 