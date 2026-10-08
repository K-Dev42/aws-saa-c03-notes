Because aws is an old service there are many types of command that can be utilized 


### aws s3
A high level way to interact with S3 buckets and objects
eg: aws s3 cp test.txt s3://myexamplebucket/test2.txt


### aws s3api
A low level way to interact with S3 buckets and objects
eg: aws s3api put-object \
--bucket text content \
-- key dir-1/my_images.tar.bz2 \
--body my_images.tar.bz2


### aws s3control 
Managing s3 access points, S3 outposts buckets, S3 batch operations, storage lens. 
eg: aws s3control describe-job \ 
-- account-id 123456789012 \
-- job-id etc 


### aws s3outposts
Manage endpoints for S3 outposts 
eg: aws s3outposts create-endpoint \
--outpost-id "a random string" \
--subnet-id "another random string" \
--security-group-id "a third radom string" \
--access-type "private" \
--customer-owned-ipv4-pool "a random ip addess"