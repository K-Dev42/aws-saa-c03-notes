## Definition
From within your EC2 instance, you can access EC2 metadata information from the Metadata Service (MDS) via a special endpoint. 

There are two versions of Metadata Service
1. Instance Metadata Service Version 1 (IMDSv1) - a request/response method
2. Instance Metadata Service Version 2 (IMDSv2) - a session-oriented method 

> IMDSv2 was implemented after an exploit of IMDSv1 was discovered. IMDSv2 adds defense in depths attacks against open firewalls, reverse proxies and SSRF vulnerabilities

The endpoints for accessing meta data of EC2:
- IPv4: 169.254.169.254
- IPv6: [fd00:ec2::254]

There are configuration options you can configure around Meta Data:
- You can enforce the use of tokens (IMDSv2)
- You can turn off the endpoint all together
- You can specify the amount of network hops allowed

> If you are the using the version 1 and get a 401 mistake then you have to use version 2