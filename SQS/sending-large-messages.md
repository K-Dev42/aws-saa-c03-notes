To send large messages to SQS you can use the libraries:
- Amazon SQS Extended Client Library for Java/Python


These Libraries are useful for messages that are larger than the current maximum of 256 KB, with a maximum of 2 GB

Both libraries save the actual payload to an S3 bucket, and publish the reference of the stored S3 object to the SNS topic