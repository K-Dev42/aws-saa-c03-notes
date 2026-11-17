## Definition
EC2 management console allows you to observe the system log for the EC2 instance. 

This is useful for troubleshooting

> Logs can be delivered to CloudWatch Logs by installing the CloudWatch Unified agent and can be accessed through a CloudWatch Log group of the same name as the instance. 

Logs that would be collected from an EC2 instance if CloudWatch Unified Agent is running and the EC2 instance is permitted to write to CloudWatch Logs

The most important ones are:
- /var/log/cfn-init.log
- /var/log/cloud-init.log (AL1 / AL2 only)