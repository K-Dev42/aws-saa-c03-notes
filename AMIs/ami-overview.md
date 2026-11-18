## Definition
Amazon Machine Image (AMI) provides the information required to launch an instance. You can turn your EC2 instances into AMIs so you can create copies of your servers. 

An AMI holds the following information:
- A template for the root volume for the instance (EBS Snapshot or Instance Store template) eg. an operating system, an application server, and applications
- Launch permissions that control which AWS accounts can use the AMI to launch instances
- A block device mapping that specifies the volumes to attach to the instance when it's launched

> AMI are region specific

### Use cases
AMIs help you keep increamental changes to your OS, application code, and system packages.

Using **System Manager Automation**, you can routinely patch your AMIs with security updates and bake (automate the creation of AMIs) those AMIs.

AMIs are used with **Launch configurations** or **Launch templates** to manage AMI revisions

### AWS marketplace
There are a lot of good AMIs that are on the marketplace some are free and some are paid. 

### Choosing an AMI
it's important to note that the AMI ID will be different for each region. So you need to always confirm you are using the correct regional AMI ID. 

AMIs can be selected based on:
- Region 
- Operating system
- Architecture (32 bit or 64 bit)
- Launch Permissions 
- Root Device Volume
    - Instance Store (Ephemeral Storage)
    - EBS Backed Volumes

### AMI boot mode
1. Legacy BIOS (Basic input/Output System)
The traditional firmware interface for computers, which has been used for decades. it initializes hardware during the boot-up process and provides runtime services for operating systems and programs.

- No support for secure boot
- May be required in case when using legacy OS or legacy software

2. Unified Extensible Interface (UEFI)
A modern firmware interface for computers, designed to replace the older BIOS firmware interface

- Supports secure boot
- Faster startup times
- Supports drives larger than 2TB
- Pre-boot environment with Graphical UI and some network capabilities

> Unless there is a specific legacy reason you want to utilize UEFI 

### Elastic Network Adapter (ENA)
Elastic Network Adapter (ENA) supports network speeds of up to 100 Gbps for supported instance types. 