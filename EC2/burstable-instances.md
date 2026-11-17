## Definition
This is the family type that starts with T- (this is free in AWS)

Burstable instances allow workloads to handle bursts of higher CPU utilizations for very short durations

This allows AWS customers to save money overall since they do not need to upgrade their instance based on highest peak usage. 

Good to know T lines
- T4g: gravitron (ARM), cheaper than t46
- T3a: AMD EPYC, cheaper than T3
- T3: Intel Xeon Scalable, best overall
- T2: Intel Xeon, free tier due to previous generation processors 

There are two modes
1. Standard Mode (default): provides a baseline level of CPU performance with the ability to burst above the baseline using accumulated CPU credits, suitable for workloads with variable CPU usage. 

2. Unlimited mode: allows an instance to sustain high CPU performance for any period whenever required, exceeding the baseline and accumulated CPU credits, with additional charges applied for the extra CPU usage beyond the accumulated credit. 