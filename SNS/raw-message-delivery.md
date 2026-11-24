## Definition
Raw message delivery avoid having Amazon Data Firehose, Amazon SQS, and HTTP/S endpoints process the JSON formatting of messages. Or in other words this is used to send messages that exclude the current format of the message.

1. Data Firehose and SQS: 
Metadata is stripped from the published message and the message is sent as is 

2. HTTP/S endpoint:
HTTP header x-amz-sns-rawdelivery with its value set to true, indicating the message should not be formatted 