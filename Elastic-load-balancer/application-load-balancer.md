## Definition

- ALB is designed to balance HTTP and HTTPS traffic
- It operates at Layer 7 (of the OSI model)
- It has a feature called Request Routing, which allows you to add routing rules to your listeners based on the HTTP protocol.
- Supports WebSockets and HTTP/2 for real-time, bidirectional communication applications
- It can handle authorization and authentication of HTTP requests
- Can only be accessed via its hostname. If you need a static IP, forward an NLB to ALB
- AWS Web Application Firewall (WAF) can be placed in front of ALB for OWASP protection 
- AWS Certificate Manager (ACM) can be attached to listeners to serve custom domains over SSL/TLS for HTTPS
- Global Accelerator can be placed in front of ALB to improve global availability 
- Amazon CloudFront can be placed in front of ALB to improve global caching of common HTTP requests 
- Amazon Cognito can be used to authenticate users via incomming HTTP requests

Use Cases:
- Microservices and Containerized Applications
- E-commerce and Retail Websites
- Corporate Websites and Web Applications
- SaaS Applications 