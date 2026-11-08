## Definition
AWS Virtual Private Cloud (VPC) is a logically isolated virtual network 
AWS VPC resembles a traditional network you'd operate in your own datacenter

A VPC provides many different networking components

The most common reason why people use VPC is because they want to use Virtual Machines (eg EC2)

Virtual network cards eg Elastic Network Interface (ENIs) is used within a VPC to attach to different compute types (eg EC2, Lambda, ECS)

> AWS VPC is tightly coupled with AWS EC2 and *all VPC CLI commands are under aws ec2

### Core components of VPC
A VPC is composed of many different networking components:
- Internet Gateway (IGW): a gateway that connects your VPC out to the internet
- Virtual Private Gateway (VPN gateway): a gateway that connects your VPC to a private external network
- Route Tables: determines where to route traffic within a VPC
- NAT gateway: allows private instances (eg virtual machine) to connect to services outside of VPC 
- Network Access Control Lists (NACLs): acts as a stateless virtual firewall for compute within a VPC operates at the subnet level with allow and deny rules
- Security groups (SG): acts as a stateful virtual firewall for compute within a VPC operates at the instance level with allow rules

Public Subnets
Subnets allow instances to have public IP addresses

Private Subnets
Subnets that disallow instances to have public IP addesses

VPC endpoints
Privately connects to AWS support services

VPC Peering
Connecting VPCs to other VPCs

### Key features to VPC
- VPCs are region specific and they do not span regions
- You can use VPC Peering to connect VPCs across-regions
- You can create up to 5 VPCs per region
- Every region comes with a default VPC 
- You can have 200 subnets per VPC
- upto 5 IPv4 CIDR Blocks per VPC 
- upto 5 IPv6 CIDR Blocks per VPC 
- Free components: VPCs, Route Tables, NACLs, Internet Gateway, security Groups and Subnets, VPC Peering
- Components that cost money: NAT gateway, VPC endpoint, VPN gateway, Customer Gateway, IPv4 addresses, Elastic IPs, DNS hostnames