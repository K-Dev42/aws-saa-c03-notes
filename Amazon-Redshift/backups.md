## Definition
Backups are enabled by default with a 1 day retention period. Retention period can be modified up to 35 days. 

Redshift always attemps to maintain at least 3 copies of your data 
1. The OG copy
2. Replica on the compute nodes
3. Backup copy in S3 

Can asychronously replicate your snapshots to S3 in a different region