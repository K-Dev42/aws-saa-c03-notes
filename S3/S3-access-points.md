## Definition
S3 access points simplify managing data access at scale for shared dataset in S3
Basically it means that access points are "doors" to the same S3 bucket and each doors has its own permission and rules 

S3 access points are named network endpoints that are attached to buckets that you can use to perform S3 object operations like Get, Put 

Each access point has:
- Distinct permissions via an Access Point Policy
- Distinct network controls
- Distinct block public access

Network Origin
- Internet: request can come from interent
- VPC: all requests must come from specified VPC

S3 access point policy allows you to write permissions for a bucket alongside your bucket policy

An access point policy helps to move specific and complex access configuration out of your bucket policy keeping your bucket policy simple and easy to read. In other words, instead of complicated policies, we can have access points for different purposes and teams. 

# Multi-region Access Points 
A global endpoint to route requests to multiple buckets residing in different regions 

Multi-region access point will return data from the regional bucket with the lowest latency (which is just AWS global accelerator)

# S3 object Lambda access points 
Allows you to **transform the output requests of S3 objects** when you want present the data differently 

S3 object lambda access points only operates on the outputted objects, the original objects in the S3 bucket remain unmodified 
> use case: whenever we want to give out a sample of the data but we also want to control what being shared and what needs to leave out before giving other teams the data.

S3 object lambda can be performed on the S3 operations
- HEAD: information about the S3 object, but not the object contents itself 
- GET: an s3 object including its contents
- LIST: a list of s3 objects
