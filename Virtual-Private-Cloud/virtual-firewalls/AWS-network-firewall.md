## Definition
AWS Network Firewall is a stateful, managed, network firewall and IDS/IPS for VPCs

Filter outbound and inbound traffic at the perimeter of your VPC
- Filter IGW traffic
- Filter NAT gateway traffic 
- Filter VPN traffic
- Filter Amazon Direct connect traffic 

AWS network firewall utilizes the open source **Suricata** IDS/IPS software and supports Suricata compatible rules

AWS Network Firewall has multiple use-cases
- Pass traffic through only from known AWS service domains or IP address endpoints, eg Amazon S3
- Use custom lists of known bad domains to limit the types of domain names that your apps can access
- Perform deep packet inspection on traffic entering or leaving your VPC 
- Use stateful protocol detection to filter protocols like HTTPS, or an independent port is used 