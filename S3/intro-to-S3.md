# Object storage
Object storage is a data storage architecture that manages data as objects, as opposed to other storage architectures 

- S3 provides with unlimited storage
- You do not need to think about the underlying infrastructure
- The S3 Console provides an interface for you to upload and access your data

## S3 Object
Object contians your data and behaves like files
Object may consist of:
- **Key** this is the name of the object
- **Value** the data itself made up of a sequence of bytes
- **Version ID** when versioning enabled, the version of the object
- **Metadata** additional information attached to the object

## S3 Bucket
Buckets hold objects. Buckets can also have folders which in turn hold objects 
> Buckets can store individual object from 0 bytes to 5 Terabytes in size