**What is internetwork traffic privacy?**
internetwork traffic privacy is about keeping data private as it travels across different networks.

There are two main services:
1. AWS PrivateLink (VPC Interface Endpoints)
- Allow you to connect an Elastic Network Interface (ENI) directly to other AWS services eg. S3, EC2, Lambda
- It can connect to select Third-party services via the AWS Marketplace
- AWS PrivateLink can go cross-account
- Has fine-grain permissions via VPC endpoint policies
- There is a charge for using AWS PrivateLink


2. VPC Gateway Endpoint
- Allows you to connect a VPC directly to S3 (or DynamoDB) staying private within the internal AWS networks
- VPC gateway endpoint can not go cross-account
- Does not have fine grain permissions
> There is no charge to use VPC Gateway Endpoints