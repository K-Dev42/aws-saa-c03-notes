## Definition
Network Address Usage (NAU) is a metric applied to resources in your virtual network to help you plan for and monitor the size of your VPC

> NAU helps you ensure you don't run out of room in your VPC 

- Each IPv4 and IPv6 address assigned to an ENI
- Additional ENI's attached to EC2 instances: 1 NAU unit
- Prefix assigned to a network interface: 1 NAU unit
- Network load balancer per AZ: 1 NAU unit
- VPC endpoint per AZ: 6 NAU unit
- Transit gateway attachment: 6 NAU unit
- Lanbda functon: 6 NAU unit
- NAT gateway: 6 NAU unit
- EFS attached to an EC2 instance: 6 NAU unit

A normal or peered VPC can handle a certain amount of NAUs: 64,000 NAUs (default) can increase up to 256,000 (quota increase)

How to use NAUs:
- You can use NAUs to manually calculate when planning a VPC
- You can use CloudWatch NAU metrics to automatically keep track of NAUs
- You need to enable NAU monitoring on a VPC to collect metrics for CloudWatch