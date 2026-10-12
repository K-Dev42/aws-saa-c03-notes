S3 bucket policy is a resource-based policy to grant an S3 bucket and bucket objects to other Principles eg. AWS accounts, Users, AWS services. 

You can do things like: only allow a specific role to read objects with prod object tag or restict access to a particular range of IP addresses. 


The way to implement a bucket policy: 
1. Create a JSON file with the policy that you wanted
2. use this command in the terminal: aws s3api put-bucket-policy --bucket myexamplebucket --policy [the file path to the JSON file]