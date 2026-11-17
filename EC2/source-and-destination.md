## Definition
the EC2 source/destination check (when enabled), restricts an instance to only send and receive traffic where it is the source or the destination. 

    aws ec2 modify-instance-attribute \
    --instance-id something something
    --no-source-dest-check

Disabling source and destination check is useful in cases where you need an EC2 instance to pass through it like utilizing the instance for Network Address Translation (NAT)