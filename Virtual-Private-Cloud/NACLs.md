## Definition
Network Access Controls (NACLs) acts as a stateless virtual firewall at the subnet level 

Stateless mean:
- Have both ALLOW and DENY rules
- A default NACL is created with every VPC 

Each NACL contains two different sets of rules:
- Inbound rules (ingress traffic which mean entering traffic)
- Outbound rules (engress traffic which mean leaving traffic)

Subnets are associated with NACLs
A subnet can only belong to a single NACL 

> The key difference between NACL vs security groups is that NACLs have both allow and deny rule. With NACL's you could block a single IP address which you can't do with SGs 

NACLs have rules
- Each rule has a number associated with the rule which determine the order of evaluation (low number has higher priority than high)
- The highest rule can be 32766 and its recommneded to work in 10 or 100 increments