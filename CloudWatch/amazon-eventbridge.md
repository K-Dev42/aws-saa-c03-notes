## Definition
what is an event bus?
An event bus receives events from a source and routes events to a target based on rules

EventBridge is a serverless event bus service that is used for application intergration by streaming real-time data to your applications.

## Core components
- Event Bus: holds event data, define rules on an event bus to react to events. We have three types: default event bus, custom event bus, and SaaS event bus

- Producers: AWS services that emits events

- Partner Sources: third-party apps that can emit events to an event bus

- Events: data emitted by services. JSON objects that travel (stream) within the event bus

- Rules: determines what events to capture and pass to targets. (100 rules per bus)

- Targets: AWS Services that consume events (5 targets per rule)

## The ananomy of an event

The json file of an event:
    
    {
        "version": "0",
        "id": "6a7e8feb-b391-4ef7-e9f1-bf3703467718",
        "detail-type": "EC2 Instance State-change Notification",
        "source": "aws.ec2",
        "account": "121212121212",
        "time": "2020-05-22T14:22:48Z",
        "region": "us-east-1",
        "resources": [
            "arn:aws:ec2:us-east-1:123456789012:instance/i-1234567890abcdef0"
        ],
        "detail": {
            "instance-id": "i-1234567890abcdef0",
            "state": "terminated"
        }
    }

1. version: by default, this is set to 0 (zero) in all events
2. ID: a unique value is generated for every event
3. detail-type: identifies fields and values that appear in the detail field
4. source: identifies the service that sourced the event
5. account: 12 digit number identifying 
6. region: AWS region where the event originated
7. resources: JSON array contains ARNa that identify resources that are involved in the event 
8. detail: JSON object containing data provided by the Cloud Service. Can contain 50 fields nested several levels deep 

## Scheduled expression
You can create EventBridge that trigger on a schedule. You can think of it as a Serverless Cron Jobs 

All scheduled events use UTC time zone 
The minimum precision for schedules is 1 minute

EventBridge supports cron expression and rate expression

Cron expresion: very fine grain control

Rate expressions: easy to set, not as fine grained 

## CloudTrail Events
Not all AWS Services emit cloudWatch events. For those services we can use CloudTrail 

Turning on CloudTrail allows EventBridge to track changes to AWS Services made by API calls or by AWS users. 

## Event patterns 
Event Patterns are used to filter what events should be used to pass along to a target. 

You can filter events by providing the same fields and values found in the original events

## Rules
You specify up to five Targets for a single rule. Commonly targeted AWS Cloud Services:

- Lambda Function
- SQS queue
- SNS topic
- Firehose delivery stream
- ESC Task

## Schema registry
EventBridge Schema Registry allows you to create, discover, and manage OpenAPI schemas for events on EventBridge. 

What is a schema? 
A schema is an outline, diagram, or model. Schemas are often used to describe the structure of different types of data. In other words, a schema is a blueprint that describe how data should be organized 