## Definition
the default user name for an operating system managed by AWS will vary based on distribution 

This is relevant for the session manager usage. When you go in an instance for the first time, you will be the ssmuser. When using session manager you have to change the user to the **default user** in order to use ssh

Therefore we need to know the name of the default user and it is usually ec2-user