## Definition
Storage Class Analysis allows you to analyze storage access patterns of objects within a bucket to recommend objects to move between STANDARD to STANDARD_IA

- Observes the infrequent access patterns of a filtered set of data over a period of time
- You can have multiple analysis filters per bucket (upto 1000 filters)
- The results can be exported to CSV
    + Export this daily usage data to an S3 bucket
    + Use data in Amazon QuickSight for data visualization
- Provides storage usage visualizations in the Amazon S3 console that are updated daily
- After a filter is applied the analysis will be available from 24 to 48 hours
- Storage class Analysis will analyze an objects for 30 days or longer to gather enough information 