## Definition
AWS Resource Access Manager (RAM) allows you to share resources across your AWS account 

VPCs can be shared with other AWS accounts within the same region to centrally manage resources in a single VPC 

Using a shared VPC allows you to:
- Reduce the number of VPCs that you create and manage
- Separate accounts for billing and access control 
- You share VPCs by sharing subnets 
- You can share only non-default subnets

You need to create a resource share in RAM (what you're sharing)
You need to create a shared principle in RAM (who's you're sharing with)