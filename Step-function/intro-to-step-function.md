## Definition
Step functions allow you to coordinate multiple AWS services into serverless workflows or in other word creating a State Machine with micro-services

What is a state machine?
A state machine is an abstract model which decides how one state moves to another based on a series of conditions. Think of a state machine like a flow chart 

What is Step Functions?
- Coordinate multiple AWS services into a serverless workflow
- A graphical console to visualize the components of your application as a series of steps
- Automatically triggers and tracks each step, and retries when there are errors, so your application executes in order and as expected, every time
- Logs the state of each step, so when things go wrong, you can diagnose and debug problems quickly

Step Functions has two types of State Machines:
- Standard: general purpose
- Express: for streaming data 