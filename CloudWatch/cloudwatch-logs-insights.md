## Definition
CloudWatch Logs Insights enables you to interactively search and analyze your CloudWatch log data and has the following advantages:

- More robust filtering then using the simple Filter events in a Log Stream
- Less burdensome than having to export logs to S3 and analyze them via Athena 

CloudWatch Logs Insights supports all types of logs

### Discovered Fields
When CloudWatch Insight reads a logs, it will first analyze the log event and try to struture the content by generating fields that you can then use in your query. 

CloudWatch Logs Insights inserts the @ symbol at the start of fields that it generates 

Five system fields will be automatically generated: 
@message: the raw unparsed log event 

@timestamp: the event timestamp contained in the log event's timestamp field

@ingestionTime: the time when the log event was reveived by CloudWatch Logs

@logStream: the name of the log stream that the log event was added to

@log: a log group identifier in the form of account-id :log-group-name
