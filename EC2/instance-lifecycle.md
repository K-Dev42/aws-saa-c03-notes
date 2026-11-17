## Definition
Actions: this is the things that we can do that move something into a particular state
- Launch: create and start an EC2 instance based on AMI
- Stop: turn off but not delete the current EC2 instance
- Start: turn back on a previously stopped EC2 instance
- Terminate: delete the EC2 instance
- Reboot: performs a soft reboot
- Retire: notifies when an instance is scheduled for reitrement due to hardware failure or end of life; it must be replaced or migrated
- Recover: automatically recovers a failed instance on new hardware if enabled, keeping the instance ID and other configurations

States: the different states that an EC2 instance can be in
- Pending: the instance is preparing to enter the running state. An instance enters the pending state when it is launched or when it is started after being in the stopped state 
- Running: the instance is running and ready for use
- Stopping: the instace is preparing to be stopped 
- Stopped: the instance is shut down and cannot be used but it can be started back up at any time
- Shutting down: the instance is preparing to be terminated
- Terminated: the instance has been permanently deleted and cannot be started

Configuration when it comes to changing the states
- Change Termination Protection: prevent the instance from being terminated 
- Change Stop Protection: prevent the instance from being stopped
- Shutdown behavior: what should happen if the instance it shutdown to either stop or terminate 
- Auto-Recovery Behavior: whether to automatically recover an instace when a system status check failure occurs 