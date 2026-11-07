## Definition
When you send API request to AWS, you sign the requests so that AWS can identify who send them. 

Signatures do the following:
- Prevents data tampering
- Verifies the identity of the requester 

> Usually when using SDK or AWS-CLI, request are signed for you automatically. The only time you need to manually sign the request yourself is when you make a request to AWS API via HTTP. 

Not all requests require signing:
- Anonymous requests to Amazon S3
- Some API operations to STS e.g AssumeRoleWithWebIdentity 

AWS has two different protocols for signing:
- AWS signature version 2 (only for legacy customer's usecases)
- AWS signature version 4
