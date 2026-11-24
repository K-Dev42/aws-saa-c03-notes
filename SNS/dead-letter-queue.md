## Definition
SNS Dead Letter Queue (DLQ) will send failed message attempts to an SQS queue. 

Topic and Queue type need to match:
- Standard SNS Topics -> Standard SQS Queue
- FIFO SNS Topic -> FIFO SQS Queue

> A queue policy will need to be configured to allow SNS to send events to the SQS queue 