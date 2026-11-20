## General Purpose SSD volumes
- Volume type: gp2, gp3 
- Use case: most general workloads
    - Transactional workloads
    - Virtual desktops
    - Medium-sized, single-instance databases
    - Low-latency interactive applications
    - Boot volumes 
    - Development and test environment
- Durability: 99.8% - 99.9%
- Volume size: 1Gib - 16TiB
- Max IOPS 16,000 (16 KiB I/O)
- Max Throughput: 250 MiB/s for gp2 and 1000 MiB/s for gp3
- EBS Multi-attach: not supported
- NVMe Reserv: Not supported
- Boot Volume: supported

## Provisioned IOPS SSD volumes
- Volume type: io1
- Use case:
    - Workloads that require sustained IOPS performace or more than 16,000 IOPS 
    - I/O-intensive database workloads
- Durability: 99.8% - 99.9%
- Volume size: 4 GiB - 16 TiB
- Max IOPS: 64,000 (16 KiB I/O)
- Max Throughput: 1,000 MiB/s
- EBS Multi-attach: supported
- NVMe Reserv: not supported
- Boot volume: supported

- Volume type: Io2 Block Express
- Use case: 
    - Sub-milisecond latency
    - Sustained IOPS performance
    - More than 64,000 IOPS or 1000 MiB/s of throughput 
- Durability: 99.9999% 
- Volume size: 4 GiB - 64 TiB
- Max IOPS: 256,000 (16 KiB I/O)
- Max throughput: 4,000 MiB/s
- EBS multi-attach: supported
- NVMe reserv: supported
- Boot volume: supported

## Throughput Optimized HDD
- Volume type: st1
- Use case: 
    - Big data
    - Data warehouses
    - Log processing
- Durability: 99.8% - 99.9%
- Volume size: 125 GiB - 16 TiB
- Max IOPS: 500 (1 MiB I/O)
- Max Throughput: 500 MiB/s
- EBS Multi-attach: not supported
- Boot volume: not supported

## Cold HDD
- Volume type: sc1
- Use case: 
    - Throughput-oriented storage for data that is infrequently accessed
    - Where lowset storage cost important
- Durability: 99.8% - 99.9%
- Volume size: 125 GiB - 16 TiB
- Max IOPS: 250 (1 MiB I/O)
- Max throughput: 250 MiB/s
- EBS multi-attach: not supported
- Boot volume: not supported

## Magnetic
- Volume type: standard
- Use case: workloads where data is infrequently accessed
- Volume size: 1 GiB - 1 TiB
- Max thoughput: 40 - 90 MiB/s
- Boot volume: supported