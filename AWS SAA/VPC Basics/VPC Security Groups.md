- Stateful
- No explicit deny, only ALLOW, or implicit deny
	- Use NACLs to add explicit denies
- Support IP/CIDR and logical resources/references
	- You can define the source (Where you typically put an IP range) as a security group, meaning any connection that has that defined source security attached to it will be allowed/denied
	- Can also self reference security groups, meaning you define the security group you are adding rules to to itself and anything within that security group can communicate with eachother
- Attached to Elastic Network Interfaces (ENIs)