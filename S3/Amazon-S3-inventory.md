## Definition
Takes inventory of objects in an S3 bucket on a repeating schedule so you have an audit history of object changes. Basically this is a feature where you can obtain an up to date report on what object currently reside in your S3 bucket.

The output file will be put in its own S3 bucket

Frequency:
    - Daily: delivered within 48 hours
    - Weekly: First report delivered within 48 hours and then future reports delivered every Sunday

Output format:
    - CSV
    - ORC
    - Parquet

Inventory scope:
    - Specific prefixes to filter objects
    - Specific all or only current versions

> The cool thing here is you can specify additional metadata to be included in the report 