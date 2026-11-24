## Definition
Publish-subscribe pattern commonly implemented in messaging systems

In a pub/sub system the sender of messages (publisher) does not send their messages directly to receivers. They instead send their messages to an event bus. The event bus categorizes their messages into groups. 

Then receivers of messages (subscribers) subsribe to these groups

Whenever new messages appear within their subscription the messages are immediately delivered to them 

- Publishers have no knowledge of who their subscribers are
- Subscribers do not pull for messages
- Messages are instead automatically and immediately pushed to subscribers 
- Messages and events are interchangeable terms in pub/sub