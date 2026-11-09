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