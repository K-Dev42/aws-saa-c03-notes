## Definition
SNS Delivery Policy defined how SNS retries the delivery of messages when server-side errors occur.

Each delivery protcol has its own delivery policy. 

> When the delivery policy is exhausted, SNS stops retrying the delivery and discards the message unless a dead-letter queue is attached to the subscription