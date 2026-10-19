**Definition**: it is an HTTP-header based mechanism that allows a server to indicate any other origins (domains, scheme, or port) than its own from which a browser should permit loading of resources. 


- If a website and its server has the same domain name then it is called: Same origin

- If a website and its server does not have matching domain names the it is called: Cross origin

> Access is controlled via HTTP header 

**Request header** 
- Origin
- Access-Control-Request-Method
- Access-Control-Request-Headers

**Response header**
- Access-Control-Allow-Origin
- Access-Control-Allow-Credentials
- Access-Control-Expose-Headers
- Access-Control-Max-Age
- Access-Control-Allow-Methods
- Access-Control-Allow-Headers


Amazon S3 allows you to set CORS configuration to a S3 bucket with static website hosting so different origins can perform HTTP requests from your S3 static website. Basically what this means is whether or not we allow different website to make request on an S3 bucket with static website hosting. 

CORS can be either JSON and XML

An endpoint: a specific network address where you access a service or in other words the destination address that a client sends a request to. Basically the URL you need to access a website or a bucket. 