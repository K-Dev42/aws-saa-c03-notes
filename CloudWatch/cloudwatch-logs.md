## Definition
CloudWatch Logs is used to monitor, store, and access your log files. Essentially, this is a centralized log management service 

You can:
- Export your logs to S3 
- Stream to elasticsearch service (ES)
- Stream CloudTrail events to cloudwatch logs
- Log security
- Log filtering
- Log retention 
    - By default, logs are kept indefinitely and never expire. You can adjust the retention policy for each log group

### Log Groups
Log group is a collection of log streams. It's common to name log groups with the forward slash syntax:

### Log Streams
A log stream represent a sequence of events from an application or instance being monitored

### Log Events
Represent a single event in a log file. Log events can be seen within a Log Stream