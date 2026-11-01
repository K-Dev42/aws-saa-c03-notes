## Definition
When data being kept in two different place and whether the data exactly match or do not match

### Strongly Consistent 
Every time you request data (query) you can expect consistent data to be returned with x time (1 seconds)

> We will never retun you old data. But you will have to wait at least 2 seconds for the query to run

### Eventually Consistent
When you request data you may get back inconsistent data within 2 seconds 

> We are giving you whatever data is currently in the database, you may get new data or old data, but if you wait a little bit longer it will generally be up to date 

Amazon S3 offers *strong consistency* for all read, write, and delete operations (Prior to Jan 2020, S3 did not have strong consistency for all s3 operations)