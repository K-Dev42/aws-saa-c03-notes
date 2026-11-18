## Definition
An elastic load balancer (ELB) can be attached to your Auto Scaling Group (ASG)
    aws autoscaling attach-load-balancer-target-groups \
    --auto-scaling-group-name my-asg \
    --target-group-arns

- Classic load balancers are assoiated directly to the ASG but this is before

- ALB, NLB or GWLB are associated indirectly via their target groups

> An attached ELB means that the ASG can use the Load Balancer's health check instead of EC2 