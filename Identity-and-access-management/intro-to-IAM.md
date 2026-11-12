## Definition
AWS Identity and Access Mangement (IAM) can help you create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. 

- IAM policies: JSON documents which grant permissions for a specific user, group or role to access services. Policies are attached to **IAM Identities**

- IAM Permission: The API actions that can or cannot be performed. They are represented in the IAM Policy document

### IAM Identities
- IAM users: end users who log into the console or interact with AWS resources programmatically or via clicking UI interfaces

- IAM Groups: group up your user so they share the same permission levels of the group eg. Administrators, Developers, Auditors

- IAM Roles: roles grant AWS resources permission to specific AWS API actions. Associate policies to a role and then assign it to an AWS resource. eg when we have an EC2 instance, if we want it to have access to S3 then we have to attached a role 

In other word, think of it as a temporary set of permissions that an authorized entity can assume (both services and users)