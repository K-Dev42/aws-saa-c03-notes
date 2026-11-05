## Definition
Amazon S3 allows you to fetch a range of bytes of data from S3 objects using the Range header during S3 GetObject API Requests.

The code to do this

    import boto3
    s3 = boto3.client('s3')
    bucket_name = 'your bucket name'
    object_key = 'your object key'

    # Get the first 100 bytes
    byte_range = 'bytes=0-99'
    response = s3.get_object(Bucket='my bucket', Key='myobject.txt', Range=byte_range)

    # Read the partial content
    data = response['Body'].read()

- Amazon S3 allows for concurrent connnections so you can request multiple parts at the same time 
- Fetching smaller ranges of a large object also allows your application to improve retry times when requests are interrupted
- Typical sizes for byte-range requests are 8 Mb or 16 Mb 