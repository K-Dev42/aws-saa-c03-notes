## Definition
Access Keys is a key and secret required to have programmatic access to AWS resources when interacting with the AWS API outside of the AWS Management Console. 

> In others word these are AWS credentials.

Access keys have two parts:
- Access Key ID
- The secret of the access key

Good practices:
- Never share your access keys to anyone
- Never commit access keys to a codebase
- You can have two active Access Keys at all times 

The way to store and use your keys
- Key will be stored in a separate file usually in a directory called aws/credentials. In this file, there will be the dafault keys when no other profile is specified. That also mean that we can add multiple profiles (by specifying their names) with their own keys inside this folder to have access to all of them during one single work session. 

- The other method would be to use environment variables (this is ideal for when working with a non local setup) 