Server-Side encryption (SSE) is **Always on** for all new S3 objects 

1. SSE-S3: Amazon S3 manages the keys, encrypts using AES-GCM (256 bit) algorithm
    - S3 encrypts each object with a unique key
    - S3 uses envelop encryption
    - S3 automatically rotates key regularly
    - By default, all objects will have SSE-S3 applied
    - There is no additional charge for using SSE-S3

2. SSE-KMS: AWS key management service and you manage the keys
    - You first create a KMS managed key
    - You choose the KMS key to encrypt your object
    - KMS can automatically rotate keys
    - KMS key policy controls who can decrypt using the key
    - KMS can help meet regulatory compliance
    - KMS keys have their own additional costs
    - AWS KMS keys must be in the same Region as the bucket
    - To upload with KMS you need kms:GenerateDataKey
    - To download with KMS you need kms:Decrypt

3. SEE-C: customer provided key (you manage the keys)
This is when you provide your own encryption key that Amazon S3 then uses to apply AES-256 encryption to your data
    - You need to provide the encryption key everytime you retrieve object because Amazon S3 will remove that key after each request
    - There is no additional charge to use SSE-C
    - Amazon S3 will store a randomly salted Hash-based Message Authentication Code (HMAC) of your encryption key to validate future requests
    - Presigned URLs support SSE-C 

*Note*: With bucket versioning, different object versions can be encrypted with different keys
        You manage encryption keys on the client side, you manage any additional safeguards, such as key rotation in the client side



4. DDSE-KMS: dual-layer server-side encryption. Encrypts client side then server side

> Server-side encryption only encrypts the contents of an object, not its metadata