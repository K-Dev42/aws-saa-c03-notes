## Definition
Delay queues let you postpone the delivery of new messages to consumers for a number of second when your app needs more time 

> Any messages that you send to a delay queue remain invisible to consumers for the duration of the delay period

Default value: 0 seconds
Max value: 900 seconds (15 minutes)


Standard queue: per-queue delay setting will only apply the new messages in the queue 

FIFO: per-queue delay setting will apply to all messages in the queue