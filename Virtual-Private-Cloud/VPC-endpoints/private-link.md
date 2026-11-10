## Definition
AWS PrivateLink is a broader service that allows you to securely connect your VPC to: 
- Supported AWS services
- AWS services hosted in other AWS accounts 
- Supported AWS marketplace partner services
Without the need of an IGW, NAT, VPN, or AWS Direct Connect connection 

How a private link is used:
- When connecting to a service provider via private link
    - On the end of services requesting user: there will be an "interface endpoint" and you also need an "ENI" and all of this is within you VPC
    - On the other end which is your service provider: they would have to set up a "service endpoint" and they would also need a load balancer as well all within their own VPC

> PrivateLink Ready partner services allows you to access SaaS product privately, as if they were running their own VPC. Or in other words you can use private link for third party services that are not in the marketplace to have all the benefits of using a private link. 


### Interface Endpoints
Interface Endpoints are Elastic Network Interfaces (ENI) with a private IP address. They serve as an entry point for traffic going to a supported service. 


### Gateway Load Balancer Endpoints 
Gateway Load Balancer (GWLB) Endpoint powered via PrivateLink allows you to distribute traffic to a fleet of network virtual appliances

The main usage of this is accessing virtual appliances (commonly security appliances) while adding an extra layer of filter and allow us to use third party virtual appliances. In other word we can deploy, scale, and manage:
-  Firewalls
- Intrusion Detection and Prevention Systems (IDS/IPS)
- Deep Packet Inspection Systems

The traffic flow: within your VPC, you have your ENI which acts as a GWLB endpoint. Then traffic from the internet travelling through your ENI, through private link and reach the service provider's GWLB where you can access your virtual appliance. After that, traffic will flow back to you instances inside your VPC

You can obtain virtual appliances as-a-service from:
- AWS Partner Network (APN)
- AWS Marketplace

> You can send traffic to GWLB by making simple configuration updates in your VPC's route tables