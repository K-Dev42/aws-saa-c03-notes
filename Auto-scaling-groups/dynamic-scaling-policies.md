## Definition
Dynamic Scaling Policies are how much ASG should change capacity. Policies are triggered by based on Cloud Watch Alarms

There are three types of dynamic scaling policies:
- Simple Scaling
- Step Scaling
- Target Tracking

Adjustment types determines how capacity should change
- ChangeInCapacity: change capacity based on the scaling adjustment
- ExactCapacity: change capacity to an exact number
- PercentChangeInCapacity: change capacity by a percentage
*note*: adjustment types is only for Simple and Step Scaling policies

### Simple Scaling Policy
Simple Scaling Policies simply change capacity in either direction by a certain amount when a CloudWatch Alarm is triggered

Create the cloudwatch alarm for each policy
    aws cloudwatch put-metric-alarm \
    --alarm-name
    --metric-name
    --namespace
    --statisics
    --period
    --threshold
    --comparison-operator
    --dimensions
    --evaluation-periods
    --alarm-actions
    --unit percent

We also need to create both the scale-in / scale-out policy
    aws autoscaling put-scaling-policy \
    --policy-name
    --auto-scaling-group-name
    --scaling-adjustment
    --adjustment-type

> When using Simple Scaling Policy it is recommended to set a cooldown period. It is also recommended to not use Simple Scaling Policy and cooldown and instead use Step or Target Tracking policies

### Step Scaling Policy
Step Scaling Policies change capacity in either direciton by a certain amount at different thresholds (steps) when a CloudWatch Alarm is repeatedly triggered. 


### Target Tracking Scaling Policy
Target tracking scaling policy automatically scales the capacity of your ASG based on a target metric value.

Metric Types:
- ASGAverageCPUUtilization
- ASGAverageNetworkIn
- ASGAverageNetworkOut
- ALBRequestCountPerTarget
- or use a custom metric

Target Tracking Scaling Policy will create two CloudWatch alarms where as Simple and Step Scaling Policy you have to create the CloudWatch Alarms yourself (unless you're using the AWS console which it will create for you)

### Predictive Scaling Policy
Predictive Scaling Policy triggers scaling by analyzing historical load data to detect daily or weekly patterns in traffic flows

- You need a forecast 24 hour CloudWatch Data before you can create a predictive scaling policy
- Predictive Scaling Policy will continuously use the last 14 days of data to tweak the policy
- It will produce hourly forecast for capacity requirements for the next 48 hours
- It will update every 6 hours using the latest CloudWatch data