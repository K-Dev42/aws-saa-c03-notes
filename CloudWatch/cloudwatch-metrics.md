## Definition
a CloudWatch Metric represents a time-ordered set of data points and it is a variable that is monitored over time 

CloudWatch comes with many predefined metrics that are generally name spaced by AWS Service eg. 

- EC2 Per-Instance Metrics
    - CPUUtilization
    - NetworkIn
    - NetworkOut
    ...


You can create your own custom metrics using the AWS CLI or SDK

High Resolution Metrics
When you publish a custom metric, you can define the resolution as either:
- Standard resolution (1 minute)
- High resolution (< 1 minute to 1 second)

With high resolution you can track in intervals of: 
- 1 second
- 5 seconds
- 10 seconds
- 30 seconds
- Multiple of 60 seconds