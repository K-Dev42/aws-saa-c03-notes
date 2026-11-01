## Definition
S3 Presigned URLs provide temporary access to upload or download object data via URL.

> Presigned URLs are commonly used to provide access to private objects.

You can use AWS CLI or AWS SDK to generate a presigned URL. 

### Anatomy of a presigned URLs
https://mybucket.s3.amazonaws.com/myobject 
?X-Amz-Algorithm=AWS4-HMAC-SHA256
&X-Amz-Credential=YOUR_AWS_ACCESS_KEY%2F20231125%2Fus-east-1...
&X-Amz-Date=20231125T123456Z
&X-Amz-Expires=300
&X-Amz-SignedHeaders=host
&X-Amz-Signature=GENERATED_SIGNATURE

- X-Amz-Algorithm: specifies the signing algorithm, typically AWS4-HMAC-SHA256
- X-Amz-Credential: includes your AWS access key and the scope of the signature (temporary)
- X-Amz-Date: is the timestamp of when the signature was created
- X-Amz-Expires: defines the duration for which the URL is valid, in this case, 300 seconds
- X-Amz-SignedHeader: indicates which headers are part of the signing process
- X-Amz-Signature: the actual signature calculated based on your AWS secret access key, the string to sign, and the signing key