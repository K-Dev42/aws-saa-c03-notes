AWS SQS Standard queue allows you a nearly-unlimited number of transactions per second (tps)

- AWS SQS Standard Queues guarantees that a message will be delivered AT LEAST once.
- More than one copy of a message could be potentially delivered out of order 
- Provide best-effort ordering that helps ensures a message is generally delivered in the same order that it was sent 