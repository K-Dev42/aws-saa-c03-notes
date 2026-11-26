## Definition
AWS Lambda is a serverless function as a service that lets you run code without provisioning or managing servers. 

Lambda execute your code only when needed and scales automatically to a 1000 lambda functions concurrently in seconds

> You pay only for the compute time you consume. There is no charge when your code is not running 

AWS Lambda Support multiple runtimes:
- Ruby
- Python
- Java
- Go
- Powershell 
...

> Lambda is commonly used to glue different services together, so the use cases are endless 

Use cases examples:

1. Processing Thumbnails
A web service allows users to upload their profile photos. They are stored in an S3 bucket. We can set up an Event Trigger that will invoke a Lambda, which will process the Profile Photo into a Thumbnail and store it back in the bucket. 

2. Contact Email Form
A company has a contact email form that submits form data via API gateway endpoint. That endpoint triggers a lambda which validates the form data and, if valid, will save the submission in DynamoDB and send an email notification via SNS to the company 