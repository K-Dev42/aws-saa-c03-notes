## Definition
Security Groups (SG) act as a stateful virtual firewall at the instance level

Security groups are associated with EC2 instances 

Each SG contains two different sets of rules:
- Inbound rules (ingress traffic which are entering traffic)
- Outbound rules (engress traffic which are exiting traffic)

A Security Group (Sg) can contain multiple instances in different subnets since SGs are not bound by subnets but they do bound by VPC

> Security Groups only have allow rules and all traffic is blocked by default 

### Use cases
1. Allow IP Addresses
You can specify the source to be an IPv4 or IPv6 range or a specific IP 
- A specific IP for IPv4 is /32
- A specific IP for IPv6 is /128 

2. Allow to another security group
You can specify the souce to be another security group

3. Nested Security Groups
An instance can belong to multiple Security Groups, and rules are permissive (instead of restrictive). If you have one security group with no Allow and add Allow to another, it will be Allow. 

### Limits
- You can have up to 10000 security groups in a region (default is 2500)
- You can have 60 inbound rules and 60 outbound rules per security group
- 16 security groups per Elastic Network Interface (ENI) (default is 5)

Security groups do not filter traffic destined to and from the following:
- Amazon Domain Name Services (DNS)
- Amazon Dynamic Host Configuration Protocol (DHCP)
- Amazon EC2 instance metadata
- Amazon ECS task metadata endpoints
- License activations for Windows instances
- Amazon Time Sync Service
- Reserved IP addresses used by the default VPC route 