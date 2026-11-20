## Definition
Route 53 is a Domain Name Service (DNS)
think of GoDaddy or NameCheap but with integration with AWS services

You can:
- **Register** and manage domains
- Create various record sets on a domain
- Implement complex traffic flows eg. Blue/green deply, failovers
- Continuously monitor records via health checks
- Resolve VPC's outside of AWS

Use Route53 to get your custom domains to point to your AWS resources
1. Incoming internet traffic
2. Route traffic to our web app backend by ALB
3. Route traffic to an instance we use to tweak our AMI
4. Route traffic to an API gateway, which powers our API
5. Route traffic to CloudFront which serves our S3 static-hosted website
6. Route traffic to an Elastic IP (EIP) which is a static IP that hosts our company's Minecraft server 