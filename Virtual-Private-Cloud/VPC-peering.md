## Definition
VPC peering allows you to connect one VPC with another over a direct network route using private IP addresses. 

Additional facts:
- VPC peering connection is not a gateway
- VPC peering connection is not a VPN connection 
- VPC peering connection does not rely on a separate peice of physical hardware
- There is no single point of failure for communication or a bandwidth bottleneck

VPC peering can be between IPv4 and IPv6 address 
Instances on peered VPCs behave just like they are on the same network
Connect VPCs across the same or different AWS accounts and regions 
Peering uses a Star Configuation: 1 central VPC and 4 other VPCs 
No transitive peering (peering must take place directly between VPCs)

### Referecing SG in Peered VPC
You can update the inbound or outbound rules for your VPC security groups to reference security groups in the peered VPC 