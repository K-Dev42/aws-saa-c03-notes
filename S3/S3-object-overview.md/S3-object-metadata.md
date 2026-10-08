Metadata provides information about the data and not the content of the data itself. 

Metadata is useful for: 
- Categorizing and organizing data
- Providing contents about data

Metadata can be either:
- System defined 
- User defined 

### System defined metadata
**Definition**: These are data that only Amazon can control. Users usually cannot set their values for these metadata values. 

**The fields**:
- Content Type: image/jpeg
- Cache Control: max-age=3600, must-revalidate
- Content Disposition: attachment; filename='example.pdf'
- Content-Encoding: gzip
- Content-Language: en-US
- Expires: Thu, 01 Dec 2030 16:00:00 GMT
- X-amz-website-redirection-location: /new-page.html
> Although you can define content type yourself. 

### User defined metadata
User defined metadata is set by the user and must start with x-amz-meta eg.

**Access and Security**
x-amz-meta-encryption: "AES-256"
x-amz-meta-access-level: "confidential"
x-amz-meta-expiration-date: "2024-01-01"
...