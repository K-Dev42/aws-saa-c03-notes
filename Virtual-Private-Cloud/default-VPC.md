## Definition
AWS has a default VPC in every region so you can immediately deploy instances. 

A default VPC is configure by default with: 
- An IPv4 CIDR block at the address 172.31.0.0/16 this is 65536 IPv4 addresses 
- A subnet (size of / 20) for each possible Availability Zone (AZ) 4096 IPv4 addresses
- An internet Gateway (IGW)
- A default Security Group (SG)
- Create a default Network access control list (NACL)
- Default DHCP options set
- A route table with a route out to the internet via IGW 

If the default VPC is deleted, it can be recreated using the AWS CLI command:
    aws ec2 create-default-vpc --region ca-central-1

Additional fact
- You cannot restore a previous default VPC that you deleted
- You cannot mark an existing nondefault VPC as a default VPC 
- If you already have a default VPC in the region, you cannot create another one