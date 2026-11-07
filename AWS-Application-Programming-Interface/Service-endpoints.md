## Definition
To connect programmatically to an AWS service, you use an endpoint which is the URL of the entry point for an AWS web service

The format for a service endpoint (it varies per service)
- protocol (generally TLSv2 is expected but it could also be TLSv1, TLSv1.1, or HTTP)
- service-code
- region-code
- amazonaws.com (domain name)
> Typically look like this: protocol://service-code.region-code.amazonaws.com 


There are four types of Service Endpoints:
1. Global Endpoints: AWS services that use the same endpoint
2. Regional Endpoints: AWS services require you to specify a region
3. FIPS Endpoints: some endpoints support FIPS for enterprise use
4. Dualstack Endpoints: Allows IPV6 or IPV4

Some additional facts about endpoints:
- The types of Service Endpoint can be combined eg Regional, FIPS, Dualstack
- An AWS Service may have multiple different service endpoints. However, AWS CLI and AWS SDK will automatically use the default endpoint for each service in an AWS region.