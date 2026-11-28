## Definition
A node is an individual computing resource (a server) within an Amazon RedShift cluster. 

A cluster is a group of of nodes working together to store and analyze large datasets

Each node provides computing resource such as:
- CPU: processes SQL queries and calculations
- RAM: holds data and intermediate results during query execution
- Storage: stores data or provides access to managed storage, depending on the RedShift node type 

### Single node
Nodes come in sizes of 160GB. You can lauch a single node to get started with RedShift. 

### Multi-node
You can launch a cluster of nodes with Multi Node mode

1. Leader Node
Manages client connections and receiving queries

2. Compute Node
Stores data and performs queries up to 128 compute nodes

### Amazon RedShift serverless
This service allows you to run analytical workloads without manually selecting node types or specifying the number of nodes 

### Node types and sizes 
There are two types of nodes

1. Dense Compute (DC): best for high performance, but they have less storage

2. Dense Storage: cluster in which you have a lot of data 