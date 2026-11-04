## Definition
Amazon S3 supports multipart upload so you can upload a single object in a set of parts. This is useful for when you want to upload a very large file. 

Multipart upload advantages:
- Improved throughput
- In case of network fail you just need to reupload the missing parts 
- Once you start a multipart upload, you can upload parts at any time, there is no expiry time to upload 
- You can upload files while you're creating a file

> For files that are +100MB multipart upload is recommended

#### Uploading procedure
1. Create the multipart upload
2. Receive the upload ID (this is to notify that parts are from the same file)
3. Divide the large file into smaller parts then we can upload each of them
4. Once done we can tell S3 that the process has been completed

#### CLI syntax
    aws s3api create-multipart-upload \
    --bucket my-bucket
    --key 'myfile'
This is to initialize the upload 

    aws s3api upload-part \
    -- bucket my-bucket \
    --key 'myfile' \
    --part-number 1 \
    --body part01 \
    --upload-id "The id that we got from initializing"
Part can be numbered from 1 to 1000
we need to collect etags for each part

    aws s3api complete-multipart-upload \
    --bucket mu-bucket
    --key 'myfile'
    --multipart-upload [the file path to a JSON file that contain Etag corresponding to each part] \
    --upload-id "The id that we got from initializing"
This is for telling S3 that we have finished with the upload

    {"Parts":[
        {"PartNumber": 1, "ETag": "\"a-string-of-characters\""},
        {"PartNumber": 2, "ETag": "\"a-string-of-characters\""},
        {"PartNumber": 3, "ETag": "\"a-string-of-characters\""}
    ]}
