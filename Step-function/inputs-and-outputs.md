Step Functions will receive JSON event data as input and pass JSON as output 

You can manipulate this JSON payload using the following:
- InputPath: select a portion of the state input 
- Parameters: create a collection of key-value pairs that are passed as input 
- ResultSelector: manipulates a state's result before ResultPath is applied 
- ResultPath: determines what should be outputted, the input, task output or a combination 
- OutputPath: select a portion of the state output to pass to the next state 

> Amazon State Language uses JSONPath syntax to identify components of JSON

### JSONPath
JSONPath is a query language for JSON, similar to XPath for XML 