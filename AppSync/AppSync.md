## Definition
AppSync is a fully managed GraphQL service

Resolver
attached to specific fields within your types in your schema. Used to implement the state-changing operations for your query, mutation, and subscription field operations. 

API types:
- GraphQL APIs: single API from multiple data sources
- Merged APIs: a collection of Graph APIs that act as one API
    - Useful if you have multiple teams that manage their own API but you want to treat all the APIsa single API

Caching options:
- None: no caching, resolvers will always fetch from data sources
- Full request caching: cache all requests
- Per-resolver caching: specific operation or field defined in a resolver will return responses from the cache 
Caching required you to provision an on-demand instance. Its not serverless 

Authorization Types:
- API Key
- AWS IAM
- Amazon Cognito User Pools

AppSync supports custom domains
Appsync has a query editor built into the UI

Resolver Runtimes
- APPSYNC_JS (Javascript)
- VTL (Velocity Template Language)