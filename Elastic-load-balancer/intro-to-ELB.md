## Definition

**What is a load balancer?**
A physical hardware or virtual software that accepts incoming traffic and then distributes the traffic to multiple targets. They can balance the load via different rules. These rules vary based on the types of load balancers. 

Elastic Load Balancer (ELB) is a suite of load balancer used to balance/distribute traffic to multiple EC2, ECS, Fargate and EKS instances. 

Application Load Balancer (ALB) 
- Operates on the OSI layer 7 the application layer (HTTP/HTTPS)
- Capable of routing based on HTTP informaition, can leverage Web Application Firewall (WAF)

Network Load Balancer (NLB)
- Operates on the OSI layer 3/4 TCP/UDP
- Designed for large throughput of low-level traffic

Gateway Load Balancer (GWLB)
- Routes traffic to virtual appliances before traffic reaches its destination 
- Useful as a security layer for traffic in transit

Classic Load Balancer (CLB)
- Operates on OSI layer 7 and 3/4
- Does not use target groups, directly attach targets
- Previous generations of load balancer that is only used in legacy cases where clients have not moved over to ALB or NLB