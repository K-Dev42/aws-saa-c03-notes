AWS has two different configuration files in TOML format at:
~/.aws/credentials - used to store sensitive credentials eg AWS access keys and secret 
~/.aws/config - used to store generic configuration eg preferred region

Typically, the credential file will take precedence over the config file 

Important global config options
- aws_access_key_id
- aws_secret_access_key
- output
- region