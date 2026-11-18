## Creating and copying
You can create an AMI from an existing EC2 instance that is either running or stopped

    aws ec2 create-image \
    --instance-id something something
    --name 
    --reboot 

You can copy an AMi
You can copy an AMI across to another region
You can encrypt a non-encrypted AMI during the copy 

    aws ec2 copy-image \
    --source-region 
    --source-image-id
    --name
    --encrypted
    --region 

## Store and restore 
You can store an AMI in an S3 bucket, and restore from an S3 bucket

The reason you would do this is if you want to copy AMIs from one AWS partiton to another

aws partitions: logical groups of AWS regions that are isolated from other groups. In other words, it is an aws environment containing multiple regions with its own Availability Zones. 

The reason why you would use this over copy
- Cheaper long-term storage
- Lifecycle management of AMIs
- Disaster recovery 
- Auditing and compliance