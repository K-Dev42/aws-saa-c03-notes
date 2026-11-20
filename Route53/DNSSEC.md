## Definition
Domain name system security extensions (DNSSEC) are a **suite of extension specifications** by the internet engineering task force (IETF) for securing data exchanged in the domain name system (DNS) in internet protocol (IP) networks. 

> DNSSEC signing lets DNS resolvers validate that a DNS response came from Amazon Route 53 and has not been tampered with

You need to create a KSK signing key and enable it. 
    aws route53 create-key-signing-key \
    --region
    --hosted-zone-id
    --key-management-service-arn
    --name
    --status
    --caller-reference

Enabling DNSSEC is a more involved process that just the two API calls. it's important to enable DNSSEC on domains so people cannot impersonate your domain. 