- Local routes always take priority
	- Local routes are always there and match the IPv4/6 CIDR
- Route tables are attached to 0 or more subnets, subnet has to have a route table
- Route table controls where data get sent

- Internet Gateway (IGW)
	- Regionally resilient
- 1 VPC = 0 or 1 IGW, 1 IGW = 0 or 1 VPC
- Managed by AWS
- How to configure an IGW
	1. Create the IGW
	2. Attach IGW to VPC
	3. Create a custom RT 
	4. Associate that custom RT with the subnet in the VPC
	5. Create Default Routes, 0.0.0.0/0 (IPv4) and ::/0 (IPv6) with target set as IGW
	6. Subnet must have automatically allocate IPv4 addresses enabled
- AWS EC2 IPv4 is not configured in the OS with a public IP
	- The EC2 instance sends a packet with it's private IP address as the source, and it's destination IP (This can be wherever)
		- The packet is sent from the EC2 instance to the IGW, where the IGW recognizes the source IP address and modifies the packet's source IP to have the assigned public IPv4 address for that private IP
			- When the opposite happens, let's say a packet is sent to the EC2 instance, the public IPv4 is used as the destination since that's how the instance is viewed on the internet
				- When the packet reaches the IGW, the reverse happens, it translates that public IP address back to the private IP and sends it to the EC2 instance
				- The EC2 instance is NEVER aware of it's public IP address. It is entirely handled by the IGW!
				- IPv6 is stored as the public address on the EC2 instance
