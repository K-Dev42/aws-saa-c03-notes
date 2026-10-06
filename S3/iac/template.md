# AWS CloudFormation

- This is AWS's infrastucture as Code service. 

- Instead of manually creating S3 buckets, IAM roles, EC2 instances, etc. We can create a reusable template by describing our infrastucture in a file (usually as a YAML or JSON)

- Sample template that create an S3 bucket: 

AWSTemplateFormatVersion: '2010-09-09'

Description: Simple S3 bucket

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket

