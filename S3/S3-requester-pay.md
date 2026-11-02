## Definition
Requesters pay bucket option allow the bucket owner to offset specific S3 costs to the requester (the user requesting the data)

This is useful when you want to share data but not incur the charges associated with others accessing the data eg.
    - Collaborative Projects: external partners pay for their own S3 data uploads/downloads
    - Client Data Storage: clients pay for their S3 storage and transfer costs
    - Shared Educational Resources: researchers cover their S3 usage fees, not the institution
    - Content Distribution: distributors/customers pay for S3 data transfer and downloads 

This feature can be toggled on and off on AWS

All requests must authenticate involving requester pays buckets
Requester assumes an IAM role before making their request
The IAM policy will have a S3:RequestPayer condition
Anonymous access to that bucket is not allowed on buckets with Requester pay

# Requesters pay header 
Requesters must include x-amz-request-payer in their API request header for:
    - DELETE, GET, HEAD, POST, and PUT requests
    - or as a parameter in a REST request
> Basically this will automatically be included 

# Requester pay troubleshooting
When you run into an error with requesters pay it will be a 403 (forbidden request) HTTP error code will occur in the following scenario:
    - The requester doesn't include the parameter x-amz-request-payer 
    - Request authenticantion fails (something is wrong with the IAM role or IAM policy)
    - The request is anonymous
    - The request is a SOAP request (SOAP requests are not allowed with requesters pay is turned on)