## Definition

1. Listeners
Incoming traffic is evaluated against listeners. Listeners evaluate any traffic that matches the listener's port. 
- Commonly listen on port 443 or port 80

Rules (Only available for Application Load Balancer)
Listeners will then invoke rules to decide what to do with the traffic 
Generally, the next step is to forward traffic to a Target Group
More advanced rules around HTTP request information in only for ALB since it operates on the OS 7 layer

2. Target Groups (Not available for Classic Load Balancer)
Are a logical grouping of possible targets such as specific EC2 instances, IP addresses 
