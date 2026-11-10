## Definition
AWS VPN lets you establish a secure and private tunnel from your network or device to the AWS global network

### AWS Site-to-Site VPN
Securely connect on-premises network or branch office site to VPC
Allows you to connect your VPC to your on-premise network

The flow of traffic
- We start from the premise, the data we go through the router on the premise and leave through the "customer gateway" (CGW) and into the VPN tunnel. On the other side of the tunnel is the VPN gateway (virtual private gateway) that is part of VPC. The traffic then will be routed by the route table and arrive at the EC2 instance on the AWS network. 

- The customer gateway device: a physical device or software application on your side of the Site-to-Site VPN connection that is the actual customer gateway itself in the network

- Target gateway: a generic term for the VPN endpoint on the Amazon side of the Site-to-Site VPN connection
- Virtual private gateway (VGW): VPN endpoint on the Amazon side of your Site-to-Site VPN connection that can be attached to a single VPC 

- Transit gateway: a transit hub that that can be used to interconnect multiple VPCs and on-premises networks, and as a VPN endpoint for the Amazon side of the Site-to-Site VPN connection. This is particularly useful if you want to enable IPv6. 

- Pricing:
    - Each VPN connection hour
    - Data transfer out from Amazon EC2 to the internet

- When talking about redundancy, Site-to-Site vpn do have 2 tunnel that if one fail then we can rely on the other tunnel to maintain the connection 

#### Virtual Private Gateway (VGW)
When you create a VGW you need to assign it an Amazon Autonomous System Number (ASN) or custom ASN (if you do not set one then it will be set to the Amazon one which is 64512)

One you create a VGW you can't change the ASN

**What is an ASN?**
An autonomous system number (ASN) is a unique identifier that is globally allocated to each autonomous system (AS) that participates in the internet. In other words it is a way for your device to be detected 

#### Customer Gateway (CGW)
A customer gateway is a resource that you create in AWS that represents the customer gateway device in your on-premise network

When you configure your CGW you'll set:
- BPG ASN for your customer gateway device
- IP address of customer gateway external device 
- Private certificate provisioned by AWS Certificate Manager (ACM)

> You will also need to provide additional configuration to your customer gateway device which will establish the connection between AWS and your on-premise network

Typical requirements that can be configured
- Internet key exchange (IKE) association 
- IPsec security association
- Tunnel interface
- (Optional) Border Gateway Protocol (BGP) peering

#### Transit Gateway for VPN
A transit gateway is a transit hub that you can use to interconnect your VPCs and your on-premises netoworks 
Transit gateway can either support either IPv4 and **IPv6** traffic inside the VPN tunnel

- Transit gateway leverages AWS Resource Manager (RAM)
- Operates as a virtual router at the regional level
- You can attach up to 5000 VPC to each pathway. An ENI will be provisioned in target VPC to facilitate communication 
- You can attach your AWS VPN connection to a transit gateway 
- You can attach Direct Connect Connections to a transit gateway
- You can attach third-party virtual appliance via transit gateway attachments 
- You can peer connect with other transit gateways 


### AWS Client VPN
Securely connect users to AWS or on-premises networks 
AWS client VPN is a fully managed client-based VPN service that enables you to secure access AWS resources and resources in your on-premises network 

The flow of traffic
- When you are on your local machine and want to connect to a VPC that you own you can use AWS client VPN to route traffic through and access your resource in a secure manner. You would use your "Open VPN Client" to connect to "AWS client VPN" after that you can access your VPC. 

Things you can use to encrypt your data:
- Certificate based authentication (mutual authentication)
- Active Directory authentication (AWS Directory Service)
- Federation authentication (Single-Sign-On SAML)

Additional facts:
- AWS Client VPN uses a single tunnel
- Use Security Groups for granular control 
- Use AD groups for granular control 
- Self-service portal to download AWS VPN desktop client 

AWS VPN client has two roles:
- Administrators: responsible for setting up and configuring the service
- Clients: the person who connects to the Client VPN endpoint to establish a VPN session

> You could use AWS client VPN to securely connect to an RDS instance that is only in a private subnet

### IPSec definition
Internet Protocol Security (IPSec) is a secure network protocol suite that authenticates and encypts the packets of data to provide secure encrypted communication between two computers over an Internet Protocol network. It is used in virtual private network (VPNs)
