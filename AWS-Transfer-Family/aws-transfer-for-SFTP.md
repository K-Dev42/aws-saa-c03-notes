## Definition
AWS Transfer Family offers fully managed support for the transfer of files over SFTP, AS2, FTPS, AND FTP directly into and out of Amazon S3 or Amazon EFS 

- FTP (File Transfer Protocol): an early network protocol without encryption, ued for transfering file over a network 

- SFTP (Secure File Transfer Protocol): uses SSH to provide a secure encrypted connection for transderring files

- FTPS (FTP Secure or FTP-SSL): extends FTP with support for SSL/TLS encryption

- AS2 (Applicability Statement 2): enables secure and reliable messaging over HTTP/S, often used for EDI (Electionic Data Interchange) transacions. Used in industries like e-commerce and retail that require proof of compliant data transfers

Common port for these protocols:
- FTP: port 20 and port 21
- SFTP: port 22
- FTPS: port 990
- AS2: port 443

### Transfer family managed file transfer workflows
Transfer family managed file transfer workflows (MFTW) is a fullt managed, serverless File Transfer Workflow service to set up, run, automte, and monitor processing of files uploaded using AWS Transfer Family

Workflow allow you to perform the following after a file is uploaded:
- Copy file: copy to another S3 destination
- Tag file: apply metadta tagging for S3
- Delete file: delete file from S3 or EFS
- Custom file-processing Step: pass file to a lambda to be processed
- Decrypt file: automatically decrypt file using PGP after uploaded to S3 or EFS 