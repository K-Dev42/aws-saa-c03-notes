## Definition
Elastic Block Store (EBS) is a highly available and durable solution for attaching persistent block storage volumes to an EC2 instance. Think of it as an external hard drive that you attach to an EC2 instance

Volumes are automatically replicated within their Availability Zone (AZ) to protect from component failure.

The types of volumes you can deploy:
- General Purpose SSD (gp2): for general usage without specific requirement
- General Purpose SSD (gp3): up to 20% lower cost per GB than gp2 
- Provisioned IOPS SSD (io1): when you require really fast input and output
- Provisioned IOPS SSD (io2): more durable than io1
- io2 block express: higher thoughput and IOPS and support larger storage capacity
- Cold HDD (sc1): lowest cost HDD volume for infrequently access workloads
- Throughput Optimized HDD (st1): magnetic drive optimized for quick throughput
- Magnetic (standard): previous generation HDD

What is IOPS?
IOPS stands for input/output per second. It is the speed at which non-contiguous reads and writes can be performed on a storage medium. High I/O =lots of small, fast reads and writes

What is Throughput?
The data transfer rate to and from the storage medium in megabytes per second

What is Bandwidth?
Bandwidth is the measurement of the total possible speed of data movement along the network

> Think of bandwidth = Pipe and throughput = water 

