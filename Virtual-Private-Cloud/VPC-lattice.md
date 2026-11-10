## Definition
Amazon VPC Lattice is a fully managed application networking service that you use to connect, secure, and monitor the services for your application. Or in other words, it is a way for different micro-services in different VPC or account to connect to each other. 

> Easily turn your AWS resources into services for a micro-service architecture

- Can be used in a single VPC
- Can be used across multiple VPC
- Can be used across accounts and used with multiple accounts
- Performs NAT for IPv4, IPv6, and overlapping networks
- Intergrates with IAM
- Weight routing for traffic eg blue/green or canary style deployments 
- Uses HTTP/S for service to service communication
- Supports custom domain names
- You can bring-you-own SSL/TLS certificate

### VPC Lattice components
- Service Network: the logical container for all services which can communicate with each other in the associated VPCs
- Listener: 
    - The protocol and port the service listens to 
    - A service can have up to 2 listeners 
    - A listener containing routing rules and has a default rule
- Target group: a collection of resources of a specific type. EC2, IP addresses, Lambda Functions, ALBS, K8s pods
- Service Directory: a central registry of all VPC Lattice services that you own or are shared with your account through AWS Resource Access Manager (AWS RAM) 