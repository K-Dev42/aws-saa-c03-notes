## Definition

- CLB is AWS's first load balancer (legacy)
- Can balance HTTP, HTTPS, or TCP traffic (not at the same time)
- It can use layer 7-specific features (OSI model) such as sticky sessions
- It can also use strict layer 4 (OSI model) balancing for purely TCP applications

> Not recommended for use, instead use NLB or ALB