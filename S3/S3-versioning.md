## Definition 
S3 versioning allows you to store multiple versions of S3 objects. 
- Stores all versions of an object in S3 at the same object key address
- By default, S3 versioning is disabled on bucket, and you must explicitly enable it
- Once enabled, it cannot be disabled, only suspended on the bucket
- Fully integrates with S3 Lifecycle rules
- MFA Delete feature provides extra protection against deletion of your data

With versioning you can recover more easily from unintended user actions and applications failures.

Versioning-enabled buckets can help you recover objects from accidental deletion or overwrite.

Buckets can be in of three states:
1. Unversioned (default)
2. Versioned 
3. Versioned Suspended 