## Definition
Route tables (RT) are used to determine where the network traffic is directed

A route table contain a set of routes
- Each route has a destination and target

Each subnet in your VPC must be implicitly or explicitly associated with a route table
A subnet can be associated with one route table at a time. But, we can associated multiple subnets with the same route table. 

### Main Route Table
A default route table created alongside every VPC and cannot be deleted
A subnet that is not explicitly associated with a route table will use the main route table

Use cases for custom route table is when you want your private resource have access to one another

**Destination**: where the route will go. Here you will specify an Ipv4 or IPv6 CIDR block or managed prefix list:
- For the internet: it is going to be the default IP addresses (the ones where all of the number are zeros)

**Target**
The network resource or **next hop** where AWS forwards the traffic to reach that destination
- Local: the default local route that lets associate subnets within the VPC route to the other route
- Internet Gateway (IGW): ingress and egress connnections to the internet for IPv4 and IPv6
- Virtual Private Gateway (VPG): out from private connection to a on-premise network
- NAT Gateway: egress connections for private instances out to the internet for IPv4
- Egress only Internet Gateway: egress connections for private instances out to the internet for IPv6
- Instance: out from a specific EC2 instance
- Network Interface (ENI): out from a specific Elastic Network Interface
- Carrier Gateway: out from AWS partnered telecom carrier networks via AWS wavelength
- Core network: out from managed wide-area networking (WAN) via AWS cloud WAN
- Gateway Load Balancer Endpoint: out from a gateway load balancer (GWLB); GWLB is for third-party virtual appliances
- Outpost Local Gateway: out from an outpost, a physical server rack with AWS services in your own datacenter
- Peering Connection: out from another Virtual Private Cloud (VPC)
- Transit Gateway (TGW): out from a transit hub for connecting multiple VPCs and on-premises network