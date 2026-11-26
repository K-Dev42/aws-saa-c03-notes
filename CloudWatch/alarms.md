## Definition
A CloudWatch Alarm monitors a CloudWatch Metric based on a defined threshold.

Metric Alarm states
- OK: the metric or expression is within the defined threshold
- ALARM: the metric or expression is outside of the defined threshold
- ISUFFICIENT_DATA: 
    - The alarm has just started
    - The metric is not available
    - Not enough data is available 

### The ananomy of an alarm
1. Threshold condition: defines when a datapoint is breached

2. Metric: the actual data we are measuring

3. Period: how often it checks to evaluate the alarm

4. Datapoint to alarm: 1 data point is breached in an evaluation period going back 4 periods (this is what trigger the alarm)


### Conditions
When you create an alarm you define the threshold
The most common type is a Static Threshold

Then you define the condition of the alarm 

### Composite alarms
Composite Alarms are alarms that watch other alarms

Using composite alarms can help you reduce noise 