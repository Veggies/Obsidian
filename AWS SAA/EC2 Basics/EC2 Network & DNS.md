- ENI (Elastic Network Interface)
	- Mac Address
	- Primary IPv4 Private IP
	- 0 or more secondary IPs
	- 0 or 1 Public IPv4
		- IP address will change if the instance is stopped then started (not restarted) or when the instance is moved
			- allocated a public DNS name
				- inside the VPC it will resolve to the private IP
	- 1 Elastic IP per private IPv4
		- removes the public IPv4 and replaces it with elastic IP
	- 0 or more IPv6
	- Security groups
	- Enable or disable source/destination check
- Secondary ENIs have just as many capabilities but can be detached and reattached to a different EC2 instance

- Secondary ENI's MAC address can be used for licensing, and then swapped to another instance to retain licensing but be on a different instance
- Multiple ENIs allow an instance to be multi-home, be a part of different subnets (Within the same AZ)
- Multiple ENIs allow for different multiple security groups