## Definition
Bastion/Jumpbox is a security hardened virtual machine that provide secure access to private subnets

- Jumpboxes are just EC2 instances that are security hardened
- Access private subnet resources via SSH or RCP
- Known as Jumpboxes because you are jumping from one box to access another

NAT cannot/should not be used as bastion because it main purpose is for EC2 to have outbound internet access to get security update 

> This is similar to getting your own local machine and access using AWS client VPN. Furthermore, system manager's session manager can replace the need for Bastions 