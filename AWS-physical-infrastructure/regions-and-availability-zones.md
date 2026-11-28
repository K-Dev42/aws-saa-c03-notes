AWS operates data centers around the world. Rather than treating all those data centers as one giant system, AWS organizes them into geographical groups called Regions.

Each regions contain multiple physically separated groups of data centers called Availability Zones 

## Definitions

What is a region?
A region is a separated geographical area where AWS operates its cloud infrastruture

> You can choose a region based on factors such as proximity to users, cost, regulatory requirements, and service availability

What is an availability zone?
An availability zone is an isolated location within a region, consisting of one or more data centers 

> The main idea when it comes to region and AZs are fault tolerance and high availability

For example, a website that is hosted by only one EC2 instance in one region will have the likely scenario of going offline if that AZ is offline. 

### Backups
An important concept to be aware when dealing with multi-AZs is they do not replace the need for backups 

eg. If someone accidentally deletes important data, that deletion may be replicated too 