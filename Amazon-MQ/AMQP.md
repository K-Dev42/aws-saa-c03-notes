## Definition
Advanced Message Queuing Protocol (AMQP) is an open standard wire-level protocol designed for messaging middleware that enables conforming client applications to communicate with conforming messaging middleware servers

- Messages are published to Exchanges
- Exchanges distriute message copies to Queues using rules called Bindings
- The Broker pushes messages to the subscribed consumers. Or the consumer pull messages from the queues
- Messages can have metadata attached to them
- Messages are only removed from the queue when a consumer ACKS (acknowledgement) the broker 

There are four types of exchanges:
- Direct exchange (default)
- Fanout exchange
- Topic exchange
- Header exchange 