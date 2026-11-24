## Definition
Message data protection safeguards the data that's published to your Amazon SNS topics by using data protection policies to audit, mask, redact, or block the sensitive information that moves between applications or AWS services

> Message data protection is only supported for standard SNS Topics

Scans for:
- Personally identifiable information (PII)
- Protected health information (PHI)
via data identofiers

You can choose to use predefined data identifiers:
- Name
- Addresses
- Credit card numbers
You can create your own data identifiers

Support the following actions:
- Audit: audit up to 99% of data published than send findings to CloudWatch, S3, or Data Firehose 
- De-identify: mask or redact data
- Deny: Block data from being sent

> Message data protection can help to reduce financial, legal, and regulatory risks by complying with privacy regulations such as HIPAA, GDPR, PCI, and FedRAMP. 