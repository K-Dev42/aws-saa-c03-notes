## Definition 

Publishing messages
The most common way to work with SNS is by having your application programmatically publish messages to the SNS Topic

To publish large messages to SNS you can use the libraries:
- Amazon SNS Extended Client Library for Java/Python 

### Message attributes
SNS supports delivery of message attributes, which let you provide structured metadata items about the message

### Message Structure
If you want to send different messages to different kinds of subscribers set message structure to json and supply a json file as the message 