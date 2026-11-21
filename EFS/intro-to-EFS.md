## Definition
Elastic File System (EFS) is a file storage service for EC2 instances
- Storage capacity grows (up to petabytes) and shrinks automatically based on the data stored (elastic)
- Multiple EC2 instances in the same VPC can mount a single EFS volume (Volume must be in the same VCP)
- EC2 instances install the NFSv4.1 client and can then mount the EFS volume
- EFS is using the Network File System version 4 (NFSv4) protocol
- EFS based per spaced used starting at $0,30 GB / month