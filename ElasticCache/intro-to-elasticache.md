## Definition
ElastiCache is a fully managed in-memory datastore for either open-source data stores Memcached or Redis which are caching engines 

### Components
- A caching engine 
is the underlying software that stores and manages the cached data. This is one of the components inside ElastiCache

- Cache nodes
Computing resources that run the caching engine in node-based deployments

- Replication
Maintains copies of data to improve availability

- Networking
VPC connectivity and security groups control network access

- Security
Authentication, encryption, and access controls

- Monitoring
CloudWatch metrics help track performance

- Backups
Snapshots and recovery for supported configurations

- Scaling
Adjust caching capacity as application demand changes

> ElasticCache is intended to cache data or HTML fragments to greatly improve response times in 10s ot 100s of milliseconds

ElastiCache can only accessible by resources in the same VPC to ensures low-latency. However, other VPC and on-premises network can also access it through private network connections such as VPC peering, transit gateway, or VPN

ElastiCache can be deployed in multiple AZs for high availablity

ElastiCache can be deployed on-premise via AWS outposts

ElastiCache can use RBAC which is a security control to regulate which service have which types of access to the cached data 

ElastiCache can be replicated cross-region via ElastiCache Global Datastores

You can reserve nodes to save money when using ElastiCache Standard 

ElastiCache can be automated to perform backups of data stores