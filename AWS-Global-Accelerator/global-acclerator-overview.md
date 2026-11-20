## Definition
AWS Global Accelerator can find the optimal path from the end user to your web-server.

Global Accelerator are deployed within Edge Locations, so you can send traffic to and Edge Location instead of directly to your web-application.

There are two types of accelerator:
- Standard: automatically route to the nearest healthy endpoint
- Custom Routing: route to specific EC2 instances

### Listeners
Listens for traffic on a specific port and sends traffic to an endpoint group

### Endpoint Groups
A collection of endpoints within a specific AWS Region
*Traffic dial* can be used to change the percentage of traffic

### Endpoints
Represents a resource to send traffic to:
An endpoint can be:
- Network Load Balancer
- Application Load Balancer
- EC2 Instances
- Elastic IP Addresses 