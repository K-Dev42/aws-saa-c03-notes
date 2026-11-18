## Definition
An AMI root device type can be either EBS-backed or Intance-backed

1. Amazon EBS-backed instances
EBS volume is automatically attached at time of launch. The storage is independent of the instance and once the instance stopped or terminated the data will still be there in the storage

2. Instance store-backed instances
The native volumes of the instances are used. When the instance is stopped or terminated all data will be lost 