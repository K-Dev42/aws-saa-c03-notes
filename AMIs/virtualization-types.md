## Definition

1. Hardware Virtual Machine (HVM)
- Full virtualization with hardware assistance
- Uses hardware-assist technology from the host system's CPU
- Potentially higher, especially for applications needing direct access to hardware
- Broader, can run unmodified operating systems. Any OS that can run on the physical hardware can run on HVM
- Can boot from an EBS volume or an instance store
- Recommended for modern operating systems and applications requiring specific hardware features 

2. Paravirtualization (PV)
- Software-assisted virtualization requiring OS modification
- Relies on a hypervisor to simulate hardware
- Initially had better performance for some workloads due to lower overhead, but has been surpassed by HVM advancements
- Limited to OSes modified for paravirtualization and can not run unmodified ones
- Can only boot from an instance store
- Historically used for certain workloads and older instance types. Less commonly used in new deployments