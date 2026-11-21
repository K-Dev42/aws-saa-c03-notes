## Definition
amazon-efs-utils package is an open-source collection of Amazon EFS tools also known as the Amazon EFS client

- EFS client enables the ability to use Amazon Cloudwatch to monitor an EFS file systems's mount status
- You need install the Amazon EFS client on an Amazon EC2 instance prior to mounting an EFS file system

> includes the Amazon EFS mount helper, which makes it easier to mount EFS file systems

EFS mount helper provides the following options:
- Mouting on supported EC2 instances
- Mouting with IAM authorization
- Mouting with Amazon EFS access points
- Mouting with an on-premise Linux client 
- Auto-mounting EFS file systems when an EC2 instance reboots
- Mounting a file system when creating a new EC2 instance
- Can mount either Linus or Mac

> Amazon EFS does not support mounting from Amazon EC2 Windows instances