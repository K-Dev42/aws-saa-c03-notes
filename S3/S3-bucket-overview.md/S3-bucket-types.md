1. General purpose buckets
- Organize data in a flat hierarchy
- The original S3 bucket type
- Recommended for most use cases
- Used with all storage classes except can't be used with S3 Express One Zone storage class
- There aren't prefix limit
- There is a default limit of 100 general buckets per account

2. Directory buckets
- Orgainizes data using folder hierarchy
- Only to be used with S3 Express One Zone storage class
- Recommmneded when you need single-digit millisecond performance on PUT and GET
- There aren't prefix limits for directory buckets
- Individual directory can scale horizontally