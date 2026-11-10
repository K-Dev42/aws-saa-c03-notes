## Definition
A gateway (in the context of cloud service) is a networking service which sits between two different network 

Gateways often act as reverse proxies, firewall and load balancer 

Gateway lists
- Internet Gateway: inbound and outbound public traffic for IPv4 and IPv6
- Egress-Only internet gateway for IPv6: outbound traffic for IPv6
- Connecting to AWS partnered telecom network
- NAT gateway: outbound private traffic for IPv4
- Virtual Private Gateway: the endpoint into your AWS account for a VPN connection
- Customer gateway: the endpoint into your on-premise account for a VPN connection
- Gateway Load Balancer (GWLB): layer 3 (network layer) load balancer to run and scale third-party virtual applications eg. firewalls, IDS/IPS 
- Direct Connect Gateway: the endpoint connection to a fiber optic connection at co-location data center
- AWS Backup Gateway: the endpoint connection for AWS managed backups
- IoT Device Gateway: the endpoint connection to send IoT data in both direction
- AWS Transit Gateway: hub and spoke model to simplify VPC peering 
- Amazon API Gateway: abstracts API endpoints to services
- AWS Storage Gateway: syncing, caching or extending local storage to cloud storage

> Some cloud services call their gateways "load balancers" or vice versa. Think gateways as an actual gate that block the flow of data between two networks