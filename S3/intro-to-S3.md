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

### S3 Object Overview
S3 objects are resources that represent data and is not infrastructure
- **Etags**: a way to detect when the contents of an object has changed without download the content
- **Checksums**: ensures the integrity of a file being uploaded or downloaded
- **Object prefixes**: simulate file-system folders in a flat hierarchy
- **Object metadata**: attach data alongside the content, to describe the content of the data
- **Object tags**: benefits resource tagging but at the object level
- **Object locking**: makes data files immutable
- **Object versioning**: have multiple versions of a data file

## S3 Bucket
Buckets hold objects. Buckets can also have folders which in turn hold objects 
> Buckets can store individual object from 0 bytes to 5 Terabytes in size.

### S3 Bucket Overview
S3 buckets are infrastructure, and they hold S3 Objects
- **S3 Bucket Naming Rule**: how we name our buckets and the best practices
- **S3 Bucket Restrictions and Limitations**: what we can and can't do with buckets
- **S3 Bucket Types**: there are two different kinds of buckets, flat (general purpose) and directory
- **S3 Bucket Folders**: how S3 buckets has virtual folders for general purpose buckets
- **Bucket Versioning**: how we can version all object
- **Bucket Encryption**: how we can encrypt the content of buckets
- **Static Website Hosting**: how we can let our buckets hold websites
> S3 is a globally available service but when you create a bucket you specify a region.