## Definition
VPC endpoints allow you to privately connect your VPC to other AWS and other services

> Think of it as a secret tunnel where you don't have to leave the AWS network

VPC endpoints provide the following benefits;
- Eliminate the need for:
    1. Internet Gateway (IGW)
    2. NAT device 
    3. VPN connection 
    4. AWS Direct Connect 
- Instances in the VPC do not require a public IPv4 address
- Traffic between your VPC and other services does not leave the AWS network
- Horizontally scaled, redundant, and highly available VPC component
- Allows secure communication between instances and services without adding availability risks or bandwidth constraints on your traffic

There are three types of VPC endpoints:
1. Interface Endpoints
2. Gateway Endpoints
3. Gateway Load Balancer Endpoints