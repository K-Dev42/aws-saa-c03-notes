1. Length: bucket names must be 3-63 characters long
2. Character: only lowercase letters, numbers, dots (.), and hyphens (-) are allowed
3. Start and end: they must begin and end with a letter or number 
4. IP addresses: not allowed
5. Adjacent periods: no two adjacent periods are allowed
6. Restricted prefixes: can't start with "xn--", "sthree", "sthree-configurator"
7. Restricted suffixes: can't end with "-s3alias" or "--ol-s3", reserved for access point alias names
8. Uniqueness: must be different and if the name has been taken then try again
9. Exclusivity: you can't have two buckets with the same name
10. Transfer acceleration: buckets used with S3 transfer acceleration can't have dots in their names 
> tldr: no uppercase, no underscores, no spaces in bucket names

### examples
mybucket123 --> valid
123.456.789.012 --> invalid because it is formatted like an IP address
My-bucket --> invalid because there is an uppercase
data.bucket..archive --> invalid because it contains adjacent periods
log-bucket --> valid
...
