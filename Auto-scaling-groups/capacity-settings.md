## Definition
The size of an Auto Scaling Group is based on: Min Size, Max Size, and Desired Capacity. 

- Min Size: the number of EC2 instances should at least be running
- Max Size: the number od EC2 instances allowed to be running
- Desired Capacity: the number of instances you would want to run on a normal basis

Updating the min and max size:
    aws autoscaling update-auto-scaling-group \
    --auto-scaling-group-name my-asg
    --min-size 2 \
    --max-size 10


Updating the desired capacity:
    aws autoscaling set-desired-capacity \
    --auto-scaling-group-name my-asg \
    --desired-capacity 2 \
    --honor-cooldown

> ASG will always launch instances to meet the minimum size capacity 