IP Masquerading
	Use a single public IP for an entire range of CIDR blocks (Private IPs)
		Because it is only using one public IP, you cannot request incoming traffic from the internet, only outgoing
	The VPC will have a route table sending all outgoing connections to the NAT Gateway, remember these IPs cannot receive incoming connections as they are all using the same public IP
		The traffic will then follow the NAT gateway's route table and be assigned the NAT gateway's IP address
			Traffic is then sent to the internet gateway, where it's source IP is again changed to the public IP that associate with the NAT gateway
NAT Gateway
	Elastic IP (Static IPv4 Public address)
	AZ resilient
		For regional resilience, need a gateway in each AZ
			And one route table for each AZ with a gateway
	Managed by AWS
	Billed based on 
		Number of gateways, billed per hour
		Data per GB

# PART 2
EC2 NAT Instance
	Must disable source/destination checks
NAT Gateways cannot use security groups
NAT Gateways do not work with IPv6
IPv6 in AWS are all publicly routables
	::/0 (All IPv6 ranges) route to IGW will allow bi-directional connectivity