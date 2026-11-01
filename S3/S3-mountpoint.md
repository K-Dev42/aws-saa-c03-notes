## Definition
Mountpoint for Amazon S3 allows you to mount an S3 bucket to your Linux local file system. 

Mountpoint is an open source client that you install on your Linux OS and provides high-throughput access to objects with basic file-system operations

Mountpoint can:
- Read files up to 5 TB in size
- List and read existing files
- Create new files

Mountpoint cannot/does not:
- Modify existing file
- Delete directories
- Support symbolic links
- Support file locking 

It can be used in the following Storage Classes
- S3 standard
- S3 Standard IA
- S3 One-Zone IA
- Reduced redundancy storage (RRS)
- S3 glacier instant retrieval

> Mountpoint is ideal for apps that don't need all the features of a shared file system and POSIX-style permissions but require Amazon S3's elastic throughput to read and write large S3 datasets. 

How to actually use Mountpoint
- Step 1: intall Mountpoint
- Step 2: create a folder
- Step 3: Mount the bucket to the folder 
- Step 4: go into the folder
- Step 5: perform basic filesystem operations
- Step 6: unmount when you are done 