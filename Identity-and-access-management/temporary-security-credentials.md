## Definition
Temporary credentials are just like Programmatic Access Keys except they are *temporary*
Temporary credentials are useful in scenarios that involves:
- identity federation
- delegation 
- cross-account access
- IAM roles

They can last from minutes to hour

They are not stored with the user but are generated dynamically and provided to the user when requested

> They are the basis for roles and identity federation. 

Everytime you use an IAM role, you would generate out an STS 

### Identity federation
The means of linking a person's electronic identity and attributes, stored across multiple distinct identity management systems. 

In other words, Identity Federation allows users to exist on a different platform. eg Users are on Facebook but gain access as if they are a user in AWS. 

IAM supports two types of identity federation
1. Enterprise identity federtation
    - SAML (Microsoft Active Directory)
    - Custom Federation broker
2. Web identity federation
    - Amazon 
    - Facebook
    - Google
    - OpenID Connect (OICD) 2.0 