## S3 bucket policies vs IAM policies 

S3 bucket policies have overlapping functionality as an IAM policy that grant access to S3.
S3 bucket policies provide convenience over IAM policies granting S3 access. 


### S3 bucket policy
- Provides access to a specific bucket and its objects
- You can specify multiple principle (users, accounts, etc) to grant access
- Bucket policies can be 20 KB in size
- Block Public Access is turned on by default and will DENY all anonymous access even if the bucket policy grant its unless the feature is turned off


### IAM policy
- Provides access to many AWS services
- Can provide permission for multiple buckets in one policy
- The principle by default is the entity the IAM policy is attached to
- IAM policy sizes are limited based on the principle: users 2KB, groups 5KB, roles 10KB 