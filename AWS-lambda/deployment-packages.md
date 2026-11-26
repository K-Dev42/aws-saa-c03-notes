## Definition
deployment package is the package which contains your function code that lambda will deploy 

Lambda supports two types of deployment packages:
- ZIP (zip archive)
- IMAGE (container image)


### Zip Archive
You ZIP the contents of your code and additional programming libraries 

AWS will upload the contents to an AWS managed S3 bucket or you upload it to an S3 bucket and reference the object to address to the lambda 

ZIP larger than 50 MB have to be uploaded to a S3 bucket first

You rely on Lambda runtimes and are limited to these runtime environments 

### Container Image
You build a container
- You need to create a Dockerfile
- You need to build the image
- You need to push the image to Amazon Elastic Container Registry (ECR)
- You reference the container image to Lambda 