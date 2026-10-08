S3 object prefixes are strings that proceed the object filename and is part of object key name. 

Since all objects in a bucket are stored in a flat-structured hierarchy, object prefixes allow for a way to organize, group, and filter objects. 

The prefixes use the forward slash "/" as a deliminator to group similar data, similar to directories (folders) or subdirectories. Prefixes are not true folders. 

> There is no limit for the number of deliminators, the only limit is the object key name cannot exceed 1024 bytes with the object prefix and filename combined. 