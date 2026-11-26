## Definition
You can use versions to manage the development of your AWS Lambda functions

eg. publish a new version of a lambda for beta testing without affecting the production version

> Each version will have its own unique ARN

When you reference a lambda function, you can reference it ARN

A Lambda has two initial versions:
- Qualified ARN: the function ARN with the version suffix
- Unqualified ARN: the function ARN without the version suffix 

> You cannot create Aliases with unqualified ARN. Unqualified ARNs points to the latest 