## Definition
Returns a set of temporary security credentials for users who have been authenticated in a mobile or web application with a web identity provider. 

The order of access:
- The user will authenticate with the web identity provider first
- Then with the ASW-CLI, assume role using that establish web identity toward sts 
- STS will then send the temporary credentials back to the user so user can use to gain access to various AWS resources