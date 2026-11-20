## Definition
CloudFront Origin is the source where CloudFront will send requests. 

- Domain name: the address to the origin
- Origin Path: the path at the specific address

Configurations for Origins:
- S3OriginConfig
    - Amazon S3 
- CustomOriginConfig
    - AWS Elemental MediaStore Container
    - Application Load Balancer
    - Lambda function URL
    - HTTP Server eg. Amazon (EC2 or another custom origin)
    - CloudFront Origins Group

