## Definition
Some metrics you might think are tracked for EC2 instances but they are not, and require installing the cloudWatch Agent

### Host level metrics
These are what you get without installing the Agent 
- CPU usage
- Network Usage
- Disk Usage
- Status Checks
    - Underlying Hypervisor status
    - Underlying EC2 instance status 


### Agent level metrics
These are what you get when installing the Agent
- Memory utilization
- Disk Swap utilization
- Disk Space utilization
- Page file utilization
- Log collection

> The CloudWatch Agent is also used to collect various logs from an EC2 instance and send them to a CloudWatch Log Group 

#### CloudWatch Agent - Log Collection
The CloudWatch Agent can send logs running on your EC2 instance to a CloudWatch Log Group

To send logs: 
1. The agent configuration needs to be updated to include the logs
2. The CloudWatch Agent service needs to be restarted

The Agent's configuration file is located at /etc/awslogs/awslogs.conf 


#### CloudWatch Agent - Install
The Cloudwatch Agent can be installed using AWS System Manager (SSM) **run a command** onto the target EC2 instance 

The package name is called "AWS-ConfigureAWSPackage"

> You must attach the CloudWatchAgentServerRole IAM role to the EC2 instance to be able to run the agent on the instance 