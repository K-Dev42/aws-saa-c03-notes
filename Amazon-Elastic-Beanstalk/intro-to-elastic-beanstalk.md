## Definition

What is a Platform as a Service? (PaaS)
A platform allowing customers to develop, run, and manage applications without the complexity of building and maintaining the infrastruture typically associated with developing and launching an app. 

How to use elastic beanstalk
Choose a platform, upload your code and it runs with little knowledge of the infrastucture 

> Not recommened for "Production" applications 

Elastic Beanstalk is powered by a CloudFormation template setups for you: 
- Elastic load balancer
- Autoscaling Groups
- RDS Database
- EC2 instance preconfigured (or custom) platforms
- Monitoring (Cloudwatch, SNS)
- In-place and Blue/Green deployment methodologies
- Security (rotates passwords)
- Can run Dockerized environment 
