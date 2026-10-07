**Definition**: An entity tag (etag) is a response header that represent a resource that has changed (without the need to download)
- The value of an etag is generally represented by a hashing function eg. MD5 or SHA-1
- Etag are part of the HTTP protocol
- Etag are used for revalidation for caching systems

S3 objects have an etag
- etag represents a hash of the object
- Reflects changes only to the contents of an object, not its metadata 
- Etag represents a specific version of an object 
> Etags are useful if you want to programmatically detect content changes to S3 objects 

