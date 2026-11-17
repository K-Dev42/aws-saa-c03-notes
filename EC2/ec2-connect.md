## Definition
There are many ways to connect a an EC2 instance. Here are some of the more common ways:

1. SSH client (same as connecting with any other virtual machine):
- Connect from your local machine via an SSH connection using a public and private key 
- You generate the public and private key on AWS and download the public key
- Port 22 needs to be open on the Security Group to connect

2. EC2 instance connect:
- Short-lived SSH keys controlled by IAM policies, works only with Linux and not all instances.

3. Sessions Manager
- Connection to Linux or Windows Machine via a reverse connection.
- Windows will log into a PowerShell, Linux will log into Bash Shell
- No need to open ports, access can be controlled via IAM
- Supports audit tail of logins

4. Fleet Manager Remote Desktop
- Connect to a Windows Machines using RDP all within the web-browser 

5. EC2 Serial Console
- Establishes a serial connections giving you direct access for troubleshooting the underlying hardware 