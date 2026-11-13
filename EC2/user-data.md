## Definition 
You can provide a script to EC2 UserData to have Cloud Init automatically run on first boot. 

- You can provide a bash script
- You can provide a cloud config yaml file 

> Scripts must be base64 when directly using the API, the AWS CLI and console will automatically encode to base64 