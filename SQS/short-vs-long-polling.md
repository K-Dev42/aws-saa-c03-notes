## Definition
Polling is the method by which we retrieve messages from the queues

1. Short Polling (default)
- Returns messages immediately, even if the message queue being polled in empty
- When you need a message right away

2. Long Polling
- Waits until message arrives in queue or till long poll timeout expires
- When you need to save money by reducing how often you poll

WaitTimeSeconds determines polling:
- Short Polling: 0 seconds
- Long polling > 0 seconds
- Max long polling is 20 seconds 