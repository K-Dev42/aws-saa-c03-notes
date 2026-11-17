## Definition
EC2 instance profile is a reference to an IAM role that will be passed and assumed by the EC2 instance when it starts up

The idea here is to avoid passing long live AWS credentials. 

- EC2 instance profile can be associated at the time of launch or on a running EC2 instance. However, if there had not been any instance profile assumed by a running EC2 instance then a hard reboot is required.
- Only a single IAM role can be associated with an instance profile
- Changing roles is not instantious due to eventual consistency

> When you select an IAM role when launching an EC2 instane, AWS will automatically create the instance profile for you. Instance profile are not easily viewed via the AWS console. 

The way to see this is through the AWS CLI

1. Creating the instance profile
    aws cli create-instance-profile \ 
    --instance-profile-name MyInstanceProfile

2. Adding the single IAM role to the instance profile
    aws cli add-role-to-instance-profile \
    --instance-profile-name MyInstanceProfile \
    --role-name MyRole

3. Associating the instane profile to the EC2 instance
    aws ec2 associated-instance-profile \
    --instance-id something something
    --iam-instance-profile Name=MyInstanceProfile

4. List all IAM profiles
    aws cli list-instance-profiles

5. Getting information about a specific instance profile 
    aws iam get-instance-profile \
    --instance-profile-name MyInstanceProfile 