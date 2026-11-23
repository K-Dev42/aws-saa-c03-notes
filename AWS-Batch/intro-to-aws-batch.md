## Definition
AWS Batch plans, schedules, and executes your batch computing workloads across the full range of AWS compute services, can utilized Spot instance to save money.

1. Jobs: a named unit of work, eg Shell script, docker container image

2. Job Definition: defines how to run the job eg. amount of compute and memory

3. Job Queues: a collection of jobs that determine job priority

4. Job Scheduler: evaluates when, where, and how to run jobs that are submitted to a job queue 
    - Defaults to First-In-First-Out (FIFO)


AWS Batch can run jobs on:
- EC2 
- Fargate
- EKS

Array Jobs: a job that shares common parameters, such as the job definition, vCPUs, and memory

Multi-node parallel jobs: run single jobs that span multiple Amazon EC2 instanes

GPU Jobs: jobs that run on EC2 GPU-based instance types

Job Depedencies: allows you to specify a job id to another job. Only when that other job complete with the job be scheduled to process