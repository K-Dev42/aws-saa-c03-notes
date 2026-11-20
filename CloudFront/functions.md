## Definition
CloudFront Functions are lightweight edge funcitons for high-scale, latency-sensitive CDN customizations.

CloudFront Functions are cheaper, faster, but more limited than Lambda@Edge functions

There are two functions for CloudFront functions:
1. Viewer request: when CloudFront receives a request from a viewer
2. Viewer respones: Before CloudFront returns the response to the viewer

Supported languages:
- JavaScript (ECMAScript 5.1 compliant)

> Functions are deployed at Edge Locations

Use-cases:
- Cache key normalization
- Header manipulation
- Status code modification and body generation
- URL redirects or rewrites
- Request authorization

