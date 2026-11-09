## Definition
Internet Gateway (IGW) allows both inbound and outbound internet traffic to your VPC

Features of IGW:
- It works for both IPv6 and IPv4 addresses 
- Provide a target in your VPC route tables for internet-routable traffic
- Performs Network Address Translation (NAT) for instances that have been assigned public IPv4 addresses
- NAT is not needed for IPv6 because all IPv6 addresses are public

### Engress-Only Internet Gateway (EO-IGW)
Engress-Only Internet Gateways (EO-IGW) are specifically for IPv6 when you want to allow outbound traffic to the internet but prevent inbound traffic from the internet. 