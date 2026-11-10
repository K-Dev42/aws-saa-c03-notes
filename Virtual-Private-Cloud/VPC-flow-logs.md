## Definition
VPC Flow Logs allow you to capture IP traffic information through your VPC. Basically Surfshark for VPCs

Flow logs can be scoped through the following
- VPC, Subnets
- Elastic Network Interface (ENIs)
- Transit Gateway 
- Transit Gateway Attachment 

You can monitor traffic for:
- ACCEPT: traffic that was accepted
- REJECT: traffic that was rejected
- ALL: all accepted and rejected traffic

Logs can be delivered to either:
- Amazon S3 bucket
- CloudWatch Logs
- Kinesis Data Firehose 

Format of log entry for VPC flow log
1. version -the VPC Flow Logs version 
2. account-id -the AWS account ID for the flow log
3. interface-id -the ID of the network interface for which the traffic is recorded
4. srcaddr -the source IP address 
5. dstaddr -the destination IP address
6. srcport -the source of the port traffic
7. dstport -the destination of the port traffic
8. protocol -the IANA protocol number of the traffic 
9. packets -the number of packets transferred during the capture window
10. bytes -the number of bytes transferred during the capture window
11. start -the start time of the capture window
12. end -the end time of the capture window
13. action - can either be ACCEPT or REJECT
14. log-status -can either be "OK", "NODATA", "SKIPDATA"