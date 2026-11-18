## Definition
An auto scaling group (ASG) contains a collection of EC2 instances that are treated as a group for the purposes of automatic scaling and management. 

Automatic scaling can occur via:
- Capacity Settings: set the expected range of capacity
    - Manual Scaling
- Health check replacement: replace instances if they are determined unhealthy
    - EC2 or ELB Health Checks
- Scaling Policies: set complex rules to determine when to scale up or down
    - Simple Scaling
    - Step Scaling
    - Target Tracking Scaling
    - Predictive Scaling

> ASGs are used to scale EC2 instances. ECS with EC2 will work, EKS with EC2 will work. Fargate does not use ASGs

### Use case
1. Burst of traffic from the internet hits our domain
2. Route53 points that traffic to our load balancer 
3. Our load balancer passes the traffic to its target group 
4. The target group is associated with our ASG and sends the traffic to instances registered with our ASG
5. The ASG scaling policy will check if our instances are near capacity
6. The scaling policy determines we need another instance, and it launches a new EC2 instance with the associated lauch configuration to our ASG