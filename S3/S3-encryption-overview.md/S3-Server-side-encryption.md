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

3. SSE-C: customer provided key (you manage the keys)
This is when you provide your own encryption key that Amazon S3 then uses to apply AES-256 encryption to your data
    - You need to provide the encryption key everytime you retrieve object because Amazon S3 will remove that key after each request
    - There is no additional charge to use SSE-C
    - Amazon S3 will store a randomly salted Hash-based Message Authentication Code (HMAC) of your encryption key to validate future requests
    - Presigned URLs support SSE-C 

*Note*: With bucket versioning, different object versions can be encrypted with different keys
        You manage encryption keys on the client side, you manage any additional safeguards, such as key rotation in the client side

4. DDSE-KMS: dual-layer server-side encryption. Encrypts client side then server side
    - It's SSE-KMS with the inclusion of client side encryption. Therefore, it would be more accurate to call it CSE-KMS. 
    - With DSSE-KMS data is encrypted twice
    - The key used for client-side encryption comes from KMS
    - There are no additional charges for DSSE and KMS keys
    - How encryption work: 
        1. Client-side requests AWS KMS to generate a data encryption key (DEK) using CMK
        2. KMS sends two versions of the DEK to you: a plaintext version and an encrypted version
        3. You uses the plaintext DEK to encrypt your data locally and then discards it from memory
        4. Encrypted version of the DEK is stored along side the encrypted data in Amazon S3
    - How decryption work:
        1. You retrieve the encrypted daat and the associated encrypted DEK
        2. You send the encrypted DEK to AWS KMS, which decrypts it using the corresponding CMK and return the plaintext DEK
        3. Use this plaintext DEK to decrypt the data locally and then discards the DEK from memory

> Server-side encryption only encrypts the contents of an object, not its metadata

S3 bucket key
Traditionally without S3 bucket, with every object is encrypted and need its own key to decrypt. Everytime we request an object S3 has to make a request to KMS which means a lot of GenerateDataKey/Decrypt.

KMS charges on the number of requests and so this charge can add up.

S3 bucket key lets you generate a short-lived bucket level key from AWS that is temporarily stored in S3
    - This will reduce request costs by up to 99%
    - This will decrease request traffic and improve overall performance

This bucket key helps to derive object-specific key that leed to decryption without the need to request to KMS
A unique bucket-level key is generated for each requester
You can enable bucket key at the bucket level to apply it to all new objects
You can enable bucket key at the object level for specific objects 
S3 bucket key can be enabled for SSE-S3 and SSE-KMS 