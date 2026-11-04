## Definition
S3 select lets you use a Strutured Query Language (SQL) to filter content of an S3 object

    - Works with object stored in CSV, JSON, or Apache Parquet format
    - Works with objects that are compressed with GZIP or BZIP2 (for CSV and JSON object only)
    - Works on object that are server-side encrypted
        The result that you will get back will be in JSON or CSV 

It can be used in the following **Storage Classes**
    - S3 standard
    - S3 intelligent tiering
    - S3 standard IA 
    - S3 One-Zone IA
    - S3 Glacier Instant Retrieval