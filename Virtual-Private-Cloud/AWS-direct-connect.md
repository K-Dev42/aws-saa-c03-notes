## Definition
AWS Direct Connnect is the AWS solution for establising **dedicated network connections** from on-premises locations to AWS

**Direct Connect** has two very-fast network connections:
1. Lower bandwidth 50MBps-500MBps
2. Higher bandwidth 1GBps, 10GBps, 100GBps

The benefit
- Help reduce network costs and increase bandwidth throughput (great for high traffic network)
- Provides a more consistent network expirience than a typical internet-based connection (reliable and secure)

Connection Requirements:
1. Your network is co-located with an existing AWS Direct Connect location
2. You are working with an AWS Direct Connect partner who is a member of the AWS Partner Network (APN)
3. You are working with an independent service provider to connect to AWS Direct Connect 

> A co-location (aka carrier-hotel) is a data center where equipment, space, and bandwidth are available for rental to retail customers

Network Requirements:
- Your network must use single-mode fiber with either a:
    - 1000BASE-LX (1310 nm) transceiver for 1 gigabit Ethernet
    - 10GBASE-LR (1310 nm) transceiver for 10 gigabit
    - 100GBASE-LR4 for 100 gigabit Ethernet 
- Auto-negotiation for a port must be disabled for a connection with a port speed of more than 1 Gbps
    - For 1 Gbps speed auto-negotiation may or may not need to be disabled
- 802.1Q VLAN encapsulation must be supported across the entire connection, including intermediate devices 
- Your device must support Border Gateway Protocol (BGP) and BGP MD5 authentication 
- (Optional) You can configure Bidirectional Forwarding Detection (BFD) on your network 

There are three factors to pricing:
1. Capacity (port size)
    - The maximum rate that data can be transferred through a network connection
    - The larger the port size the greater the cost eg. 50,..,100GBps
2. Port hours 
    - For amount of time a Direct Connect port is provisioned for use, regardless of data transfer
    - There are two connection types:
        1. Dedicated: physical connections between your network port and an AWS network port 
            - Billed per hour via AWS 
        2. Hosted: logical connections between AWS partner and AWS network port
            - Billing is subject to the AWS Direct Connect Deliver Partner
3. Data Transfer Out (DTO)
- Charged based on outbound traffic sent through Direct Connect to destinations outside AWS 
- Data transfer in is free 
- Data transfer within the same region will not result in a cost 