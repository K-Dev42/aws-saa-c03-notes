## Definition
Environment variables (env vars) provide another way to specify configuration and credentials 

This can be useful for scripting or temporarily set a named profile as the default

The priority hierarchy (from highest to lowest):
- AWS CLI parameters
- Environment variables
- Configuration files 

Common Environment variables for AWS CLI:
- AWS_ACCESS_KEY_ID: the access key generated from programmatic access
- AWS_SECRET_ACCESS_KEY: the secret key generated from programmatic access
- AWS_DEFAULT_REGION: the default region to be used when no region is specified 
- AWS_REGION: overrides the values in the environment variable AWS_DEFAULT_REGION and the profile setting region
- AWS_PROFILE: the name of the AWS CLI profile with the credentials 