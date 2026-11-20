## Definition
Zonal shift is a capability in Amazon Route 53 application recovery controller (route 53 ARC)

> Shift a load balancer resource away from an impaired Availability Zone to healthy AZ with a single action 

- Zonal shifts are only supported on Application Load Balancers and Network Load Balancers with cross-zone load balancing turned off 

- Zonal shift isn't supported when you use an Application Load Balancer as an accelerator endpoint in AWS Global Accelerator

- You can start a zonal shift for a specific load balancer only for a single Availability Zone. You can't start a zonal shift for multiple Availability Zones 