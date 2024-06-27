- AMIs are templates for creating EC2 instances
- Regional based, unique ID per region
	- Can only be used in the region it is in
- Permissions by default the AMI is only available to your account
	- Can be set to specific accounts and public
- AMI can be created from an EC2 instance

- Lifecycle
	1. Launch
		- Use an AMI to launch an instance
	2. Configure
		- Configuring the EC2 instance to be setup perfectly for an end user or workstation
	3. Create Image
		- Create AMI from the instance and volumes attached
			- EBS snapshots are created from the volumes attached
				- AMI references the snapshots via block device mapping
					- block device mapping links device ID and snapshot ID
	4. Launch
		- Will have the same exact everything as the AMI
			- Snapshots will be used to create volumes and attached to the instance with the same block IDs as the AMI

- AMI Baking
	- Creating an AMI from a configured instance
- AMI cannot be edited, must be changed as an instance
- AMIs can be copied between regions