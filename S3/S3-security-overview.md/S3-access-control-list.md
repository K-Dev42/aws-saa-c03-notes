ACLs grant basic read/write permissions to other AWS accounts

- You can grant permissions only to other AWS accounts
- You cannot grant permission to users in your AWS account 
- You cannot grant conditional permissions
- You cannot explicitly deny permissions

S3 ACLs has been traditionally used to allow other AWS accounts to upload objects to a bucket 

> Access controls lists (ACLs) is a legacy feature of S3 and there are more robust ways to provide cross-account access via bucket policies and access points. 