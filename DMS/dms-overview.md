## Definition
AWS Database Migration Service (DMS) allows you to quickly and securely migrate one database to another. DMS can be used to migrate your on-premise database to AWS

AWS Schema Conversion is used in many cases to automatcically convert a source database schema to a target database schema.

For data warehouses you can use the desktop app AWS Schema Conversion Tool 

Migration Methods
- Homogenous data migration: migrate data with native database tools

- Instance Replication: provision an instance with chosen instance type to perform the replications between databases

- Serverless Replication (DMS Serverless): 
    - A serverless offering where you pay as you go, with some limitations: 
        - Does not have public IPs
        - Must use VPC endpoints to access specific AWS services 
        - Limited selection of possible sources and targets
        - Doesn't support views with selection and transportation rules 