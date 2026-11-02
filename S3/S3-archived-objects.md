## Definition 
Archived objects are rarely-access objects Amazon S3 that cannot be accessed in real-time in exchange for a reduced storage cost.

There are two ways to archive objects:
1. Archive Storage Classes 
    - When you know your access patterns
    - Requires manual invention to move data
    - Lower costs archive storage cost 
        S3 Glacier Flexible Retrieval: from minutes to hours
        S3 Glacier Deep Archive: +12 hours

2. Archive Access Tiers
    - When you don't know your access pattern
    - Automatically move data 
    - Slightly higher cost compared to archive storage classes 
        S3 intelligent-tiering archive access tier: within minutes
        S3 intelligent-tiering deep archive access: +12 hours 