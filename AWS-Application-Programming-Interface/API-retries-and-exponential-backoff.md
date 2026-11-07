## Definition
When interacting with APIs over a network, it's common for a networking issue to occur for various reasons due to the amount of devices a request has to pass through and points of failures:
- DNS servers
- Switches
- Load balancers

When working with APIs you need to plan for possible network failures by **trying again**

> It is an industry standard for APIs to use an exponential backoff before trying again

When a request fail, these are the amount of time we have to wait until we try again. The time will increase proportional to the amount of attempts that has been done
- Try again in 1 second
- Try again in 2 seconds
- Try again in 4 seconds
- Try again in 8 seconds
- Try again in 16 seconds
- Try again in 32 seconds

> A good CLI or SDK will have exponential backoff built in with options like how many times it should try