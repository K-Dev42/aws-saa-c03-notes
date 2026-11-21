## Definition
AWS backup allows you to centrally manage backups across AWS services. 

Backup services:
- Amazon S3
- VMWare VMs
- DynamoDB
- FSx file systems
- EC2
- EFS
- EBS 
- RDS and Aurora
- AWS Backlnt (SAP HANNA)
- Storage gate way (SGW)
- DocumentDB
- Neptune
- Timestream
- And more...

How to use this service
1. Create a Backup Plan: A backup policy defines the backup schedule, backup window, backup lifecycle.

2. Backup Vault: Backup are stored in a backup vault 
    - AWS Backup Vault Lock allows for Write-Once-Read-Many (WORM) t set a retention period 
    - Standard Vault (default): backups are always initially stored in the standard vault
    - Air-Gapped Vault: backups can be moved to a logically air-gapped vault for additional security
- Resources can be assigned a backup plan using AWS Resource Tags
- You can backup resources to other AWS Regions or AWS Accounts
- You can manage backups from a centralized accont across your entire AWS organization
- Backups are incremental, so you only store the difference instead of full backups to save costs
- AWS Backups can use an independent KMS encryption key from that of your AWS resources
- Associated charges for AWS backup appear as "backup" under Cost Explorer 

> AWS Backup Audit Manager us built-in reporting and auditing for AWS Backups