## Definition
Record sets are a collection of records which determine where to send traffic

Record sets are always changed in batch via the API

The following record types supported by Route53
- A record type
- AAAA record type
- CAA record type
- CNAME record type
- DS record type
- MX record type
- NAPTR record type
- NS record type
- PTR record type
- SOA record type
- SPF record type
- SRV record type
- TXT record type

### Alias Record
AWS has its own special Alias Record which extends DNS functionally. It will route traffic to specific AWS resources 

Alias records are smart where they can detect the change of an IP address and continuously keep that endpoint pointed to the correct resource
Alias Target can point to:
- CloudFront
- Elastic Beanstalk environment
- ELB load balancer 
- S3 website endpoint
- Resource record set
- VPC endpoint