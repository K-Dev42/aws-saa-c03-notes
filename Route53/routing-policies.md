There are **7 different types** of routing available inside Route53

- Simple Routing: default routing policy. multiple addresses result in a random selection
- Weighted Routing: route traffic based on weighted values to split traffic
- Latency-Based Routing: route traffic to region resource with the lowest latency
- Failover Routing: route traffic if primary endpoint is unhealthy to the secondary endpoint
- Geolocation Routing: route traffic based on the location of your users 
- Geo-proximity Routing: route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another
- Multi-value Answer Routing: responds to DNS queries with up to eight healthy records selected at random

### Simple Routing Policies
Simple routing policies are the most basic and the default policy in Route53

- You have 1 record and provide multiple IP addresses
- When multiple values are specified for a record, Route53 will return all values back to the user in a random order


### Weighted Routing Policies
Weighted Routing Policies let you split up traffic based on different 'weights' assigned

This allows you to send a certain percentage of overall traffic to one server and have any other traffic to be directed to a completely different server. 


### Latency Based Routing Policies
Latency based routing allows you to direct traffic based on the lowest network latency possible for your end-user based on region. 

Requires a latency resource record to be set for the EC2 or ELB resource that hosts your application in each region 


### Failover Routing Policies
Failover routing policies allow you to create active/passive setups in situations where you want a primary site in one location and a secondary data recovery site in another. 

Route53 automatically monitors health checks from your primary site to determine the health of end-points. If an end-point is determined to be in a failed state, all traffic is automatically directed to the secondary location. 


### Geolocation Routing Policies
Geolocation Routing Policies allow you to direct traffic based on the geographic location of where the request originated from.

Or in other word this type of routing would route to resource that is located within the same region as the request. 


### Geoproximity Routing Policies
geoproximity routing policies allow you to direct traffic based on the geographic location of your users and your AWS resources

You can route more or less traffic to a specific resource be specifying a 'Bias' value. 

Bias values expand or shrink the size of the geographic region from which traffic is routed to
You must use Route 53 Traffic Flow to use geoproximity routing policies