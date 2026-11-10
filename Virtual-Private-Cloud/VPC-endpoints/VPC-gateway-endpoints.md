## Definition
A gateway endpoint provide reliable connectivity to Amazon S3 and DynamoDB without requiring an internet gateway or a NAT device for your VPC. 

Facts:
- Gateway endpoints do not use AWS PrivateLink
- Gateway endpoints have no additional charge
- Gateway endpoints support the following services:
    - Amazon DynamoDB
    - Amazon S3

> To create a gateway endpoint, you must specify the VPC in which you want to create the endpoint and the service to which you want to establish the connection. 