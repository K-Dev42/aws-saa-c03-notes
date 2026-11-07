## Definition
**What is an Application Programming Interface (API)?**
An API is a software that allows two applications/services to talk to each other. The most common type of API is via HTTP/S requests.

AWS API is an HTTP API and you can interact by sending HTTPS requests, using an application interacting with APIs like **Postman**
> The idea here is you will get back a response of infomation about your cloud resources 

    GET / HTTP/1.1
    x-amz-target: GraniteServiceVersion201...
    x-amz-date: a bunch of random character 
    Authorization: AWS4-HMAC-SHA256...
    Content-Type: application/json
    Accept: application/json
    Content-Encoding: amz-1.0
    Content-Length: 45
    Connection: keep-alive

Info about the components of the code block above:
- This is a get request using HTTP
- Each AWS services has its own endpoint that you can send requests
- Furthermore, these request must the authenticated via **signed request** 
- To acquire the token to make a signed request we need to request that token using AWS credentials 
- You also need to provide an action and accompanying parameters as the payload 

Rarely do users directly send HTTP requests directly to the AWS API. it's much easier to interact with the API via a variety of Developer Tools
- AWS mangement console (on the browser)
- ASW SDK (interact with the API using other programming languages)
- AWS CLI (interact with API via terminal/shell program)