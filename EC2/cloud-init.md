## Definition
Cloud-init is the industry standard multi-distribution method for cross-platform **cloud instance initialization**. It is supported across all major public cloud providers, provisioning systems for private cloud infrastruture, and bare-metal installations. 

What is Cloud Instance Initialization?
The process of preparing an instance with configuration data for the operation system and runtime environment. 

Cloud instances are initialized from a disk image and instance data:
- Meta-data
- **User-data**
- Vendor-data

User Data is a script that you want to run when an instance first boot up eg. Intall Apache web-server

AWS EC2 supports for cloud-init across most Linux Distros that support it