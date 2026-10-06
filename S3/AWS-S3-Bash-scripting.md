# Create Bucket
#!/usr/bin/env bash

aws s3api create-bucket --bucket [bucket-name]

# Delete Bucket
#!/usr/bin/env bash

aws s3api delete-bucket --bucket [bucket-name]

# List Object
#!/usr/bin/env bash

aws s3api list-object-v2 --bucket [bucket-name]




