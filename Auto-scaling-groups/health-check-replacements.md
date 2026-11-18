## Definition
Health check replacement is when an ASG replaces an instances if that instance was unhealthy. There are two types of health checks ASG can perform 

1. EC2 Health Check
If the EC2 instance fails either of its EC2 status checks

2. ELB Health check
ASG will perform a health check based on the ELB health check. ELB pings an HTTP endpoint at a specific path, port and status code 