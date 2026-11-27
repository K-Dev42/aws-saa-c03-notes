ElastiCache has two deployment options:
- ElastiCache (standard mode directly managing nodes in a cluster)
- ElastiCache Serverless

### Serverless
- Use case: unpredictable workloads
- Management: Automatically scales
- Billing:
    - Data stored
    - ElastiCache Processing Units (ECPUs)

### Standard
- Use case: predictable workloads
- Management: Customer manages cluster and nodes
- Billing:
    - Based on number of nodes
    - based on node type (size of node)

> Standard can be deployed on-premise via AWS Outposts