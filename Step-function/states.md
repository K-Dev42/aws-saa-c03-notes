## Pass state
Passes its input to its outpust, without performing work (dummy/lock). Pass states are useful when constructing and debugging state machines 

## Task state
Represent a single unit of work performed by a state machine 

A task performs by
1. An AWS Lambda function 
2. Or passing parameters to the API actions of other services
3. Or using an activity

## Choice state
Add branching logic to your state machine 

## Wait state
Delays the state machine from continuing for a specified time 

## Succeed state
Stop an execution successfully 

## Fail state 
Stop the execution of the state machine and marks it as a failure 

## Parallel states
Can be used to create parallel branches of execution in your state machine

The state machine does not move forward until both states complete 

## Map state
Allow you to iterate over an array 