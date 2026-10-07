S3 general purpose bucket does not hae true folders.

When you create a folder in the S3 console, Amazon S3 creates a zero byte S3 object with a name that ends with a forward slash eg. myfolder/

### Folder characteristics
- S3 folders are not their own independent identities but just S3 objects
- S3 folders don't include metadata, permissions
- S3 folders don't contain anything, they can't be full or empty
- S3 objects are not "moved into" a folder but instead they should just be renamed to contain the folder name as a prefix 