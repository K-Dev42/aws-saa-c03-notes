A checksum is used to check the sum (amount) of data to ensure the data integrity of a file. If data is downloaded and if in-transit data is loss or mangled then the checksum will determine there is something wrong with the file. 
> Basically checksum check is there is something wrong with the file itself. 

Amazon S3 offers the following checksum algorithms
- CRC32 (Cyclic Redundancy Check)
- CRC32C 
- SHA1 (Secure Hash Algorithms)
- SHA256 