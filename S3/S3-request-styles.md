When making requests by using the REST API there are two styles of request: 
1. Virtual hosted-style requests: the bucket name is a subdomain on the host
2. Path-style requests: the bucket name is in the request path

---

### Virtual hosted-style request

DELETE /puppu.jpg HTTP/1.1
Host: **examplebucket**.s3.us-west-2.amazonnaws.com
Date: Mon, 11 Apr 2016 12:00:00 GMT
Authorization: authorization string 

---

### Path-style request 

DELETE /**examplebucket**/puppy.jpg HTTP/1.1
Host: s3.us-west-2.amazonaws.com
Date: Mon, 11 Apr 2016 12:00:00 GMT 
x-amz-date: Mon, 11 Apr 2016 12:00:00 GMT 
Authorization: authorization string

---

> Although S3 supports both request styles, the Path-style URLs will be dicontinued in the future 