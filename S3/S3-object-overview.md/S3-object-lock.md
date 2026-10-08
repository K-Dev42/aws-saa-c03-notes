S3 object locks allows to prevent the deletion of object in a bucket 

Object lock is for companies that need to prevent object being deleted to have:
- Data integrity
- Regulatory compliance 

S3 object lock is **SEC 17a-4**, **CTCC**, and **FINRA** regulation compliant
> S3 buckets with object lock can't be used as destination buckets for server access log

Object locking setting can only be set via the AWS API eg. (CLI, SDK) and not the aws console. The reason for this is to avoid misconfiguration by non-technical users. 