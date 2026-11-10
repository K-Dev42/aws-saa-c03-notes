## Definition of NAT
A method of mapping an IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic-routing device. 

In other word, private IP addresses in private subnets need to translate into a public IP address in order to have traffic route from and back to the internet. 

Another thing that we can use NAT for is if you have two network that have conflicting network addresses, you can use a NAT to make the addresses more agreeable 

### NAT Gateway
A NAT Gateway is a fully managed NAT service to allow instances in your private subnet to establish outbound connections
- A NAT Gateway in redundant within a single subnet meaning you need a NAT gateway per subnet

The cost of NAT gateway:
- you pay $0.045 per hour per NAT Gateway
> NAT gateway can be expensive really quickly

NAT Gateway has two connection modes:
- Public (Default)
    - Instances in private subnets can connect to the internet through a public NAT gateway 
    - cannot receive unsolicited inbound connections from the interent 
    - You must associate an Elastic IP (EIP) address 
- Private 
    - Instances in private subnets can connect to other VPCs or your on-premises network through a private NAT gateway 
    - You can route traffic from the NAT gateway through a transit gateway or a virtual private gateway 
    - You cannot associate an elastic IP address with a private NAT gateway 

### DNS64 and NAT64
A NAT gateway supports network address translation from IPv6 to IPv4, popularly known as NAT64

**What is DNS64**
Your IPv6 workloads running in VPCs can only send and receive IPv6 network packets. Without DNS64, a DNS query for an IPv4-only service will yeild an IPv4 destination address in response and your IPv6-only service cannot communicate with it. To bridge this communication gap, you can enable DNS64 for a subnet and it applies to all the AWS resources within that subnet. 

**What is NAT64**
NAT64 enables your IPv6-only services in Amazon VPCs to communicate with IPv4-only services within the same VPC (in different subnets) or connected VPCs, in your on-premises networks, or over the internet.

In other words:
- DNS64 helps IPv6-only devices discover IPv4-only services
- NAT64 translates IPv6 traffic into IPv4 traffic, allowing IPv6-only instances to communicate with IPv4-only services
- These two work together: DNS64 synthesize an IPv6 addresses for the IPv6 EC2 instance to know where to send traffic, then the NAT64 translate the IPv6 packets to IPv4 in order for the service to understand

