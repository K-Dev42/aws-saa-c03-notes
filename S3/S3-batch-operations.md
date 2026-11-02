## Definition
S3 batch operations performs large-scale batch operations on Amazon S3 objects (billions of objects containing exabypes of data)

The follow **batch operations types** can be performed:
    - Copy: copies each object listed in the manifest to the specified destination bucket
    - Invoke AWS Lambda function: run a lambda function against each object
    - Replace all obeject tags: replaces the Amazon S3 object tags of each object
    - Replace access control list (ACL): replaces the (ACLs) for each object
    - Restore: sends a restore request to S3 Glacier
    - Object lock retention: prevents overwriting or deleting for a fixed amount of time 
    - Object Lock legal hold: prevents overwriting or deleting until the legal hold is removed 

> in order to perform a batch operation you need to provide lists of objects in an S3 or supply an S3 inventory report manifest.json. Further more, when performing a batch operation, it will generate a completion report to audit the outcome of bulk operation. 