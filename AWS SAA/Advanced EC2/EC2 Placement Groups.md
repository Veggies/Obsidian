- Cluster
	- Keep all instances on the same hardware
	- Create all instances at the same time so AWS provides capacity for all of them
	- Performance focused
	- Must all be launched in a single AZ
			- Whatever AZ the first instance is launched into is what the cluster is locked into
	- All instances have direct connections to eachother
	- Lowest latency possible and max packets per second in AWS
	- Requires supported instance
		- Use same instance type on all instances for best performance
	- 10GB/s for single stream performance
	- Use cases
		- Performance
		- Fast Speeds
		- Low latency

- Spread
	- Keep instances on separate hardware
	- Limit of 7 per AZ
	- Each instance runs on a different rack
		- Each rack has it's own network and power source
	- Does not support dedicated instances or host
	- Use case:
		- Small number of instances that must be separated from eachother

- Partition
	- Groups of instances on different hardware
	- When you have more than 7 instances in AZ that need to be spread
		- Specify a number of partition, max of 7 per AZ
		- Can put as many instances as you want in each partition
			- Placed by you or EC2
	- Great for topology aware applications
	- Contain impact of failure to part of an application