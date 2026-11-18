## Definition
ASG Termination Policies decide the order for terminating instances

AWS provides predefined policies:
- Default 
- AllocationStrategy
- OldestLaunchTemplate
- OldestLauchconfiguration
- ClosestToNextInstanceHour
- Newestinstance
- OldestInstance

> You can create a custom termination policy by invoking a Lambda Function