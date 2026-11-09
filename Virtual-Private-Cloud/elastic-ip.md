## Definition
Elastic IP (EIP) address in AWS is a static IPv4 address 
A static IP is an address that always stays the same 

**Use Case 1**
When you restart a EC2 instance its IP address will change.
This dynamic nature could break external connections relying on the IP address 

**Use Case 2**
When an EC2 instance fails you might want to use the same IP address
on a fail-over instance. An Elastic IP allows you to remap that static IP address 

Additional facts
- Elastic IPs are region specific
- Elastic IPs are drawn from Amazon's pool of IPv4 addresses
- Elastic IPs are charge $1 for each that is allocated and are unassociated (so if you use these addresses then they will not be charge)
- Elastic IPs also include the public IPv4 address charge
- Elastic IPs can be associated or unassociated to an instance eg EC2 or to a primary network card eg ENI