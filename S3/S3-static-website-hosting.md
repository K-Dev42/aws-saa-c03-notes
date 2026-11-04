## Definition
S3 static website hosting allows you to host and serve a static website from an S3 bucket 

- S3 website endpoints do not support HTTPS which can be addressed by using **Amazon CloudFront** 
- S3 Static Website hosting will provide a website endpoint

*reminder:* 
- An endpoint is the network address/URL you send a request to
- A static website is a website made of prebuilt files like HTML, CSS, Javascript, and images. There's no server generating pages dynamically for each request 

There are two types of hosting (via the console):
- Host a static website
- Redirect requests to objects

> Requesters pays do not allow access through a website endpoint