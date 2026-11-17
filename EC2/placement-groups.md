## Definition
Placement groups let you choose the logical placement of your instances to optimize for communication, performance, or durability. Placement groups are **free**. 

1. Cluster
- Packs instances close together inside an availability zone
- Low-latency network performance for tighly-coupled node-to-node communication
- Well suited for High-Performance Computing (HPC) applications
- Clusters cannot be multi-AZ

2. Partition
- Spread instances across logical partitions
- Each partitions does not share the underlying hardware with each other (rack per partition)
- Well-suited for large distributed and repliated workloads (Hadoop, Cassandra, Kafka)

3. Spread
- Each instance is placed on a different rack
- When critical instances should be kept separate from each other
- You can spread a max of 7 instances. Spreads can be multi-AZ