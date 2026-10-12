Amazon S3 Access Grants lets you map identities in a directory service (IAM identify center, Active Directory, Okta) to access dataset is S3.

1. Access grant instance: a logical container for individual grants
2. Locations (S3://): determines which bucket data you access
3. Grants: the granular scope of access within a location eg.
    - Level of access:
        READ
        WRITE
        READWRITE

    - What will have access
        IAM role
        IAM user

    - Bucket objects
        mybucket/scifi/*

> These are temporary access grants that provides just-in-time permission to people that have already use a directory service to access data within a bucket. 