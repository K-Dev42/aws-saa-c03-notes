## Definition
S3 transfer acceleration is a bucket-level feature that provides fast and secure transfer of files over long distances between your end users and an S3 bucket. 

> Utilized Cloudfront's distributed Edge locations to quickly enter the Amazon Global Network 

Instead of uploading to your bucket, users use a distinct endpoint to route to an edge location 
- Only supported on virtual-hosted style requests
- Buckets cannot contain periods and must be DNS compliant 
- It can take 20 minutes to enable Transfer Acceleration