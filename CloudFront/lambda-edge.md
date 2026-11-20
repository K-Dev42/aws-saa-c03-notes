## Definition
Lambda@Edge are lambda functions to override the behaviour of requests and responses

There are 4 functions for Lambda@Edge
1. Viewer request: When CloudFront receives a request from a viewer
2. Origin request: Before CloudFront forwards a request to the origin
3. Origin response: When CloudFront receives a response from the origin
4. Viewer respone: Before CloudFront returns the response to the viewer

> Functions are deployed at Regional Edge Caches

Supported languages:
- Python
- Node.js 


Viewer Request Use-Cases
- Redirect HTTP for HTTPS 
- Inspect cookies for user authentication
- Modify headers for A/B testing

Viewer Response Use-Cases
- Add security headers (eg. CSP, HSTS)
- Set cookies for client-side tracking
- Customize error messages 

Origin Request Use-Cases 
- Rewrite URLs for SEO or routing
- Inject headers for origin authentication
- Selective content serving based on user-agent

Origin Response Use-Cases
- Modify headers to control caching
- Update URLs in HTML for versioning
- Customize error responses from the origin