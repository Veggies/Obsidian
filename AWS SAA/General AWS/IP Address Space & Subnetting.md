0.0.0.0 > 255.255.255.255 = ~4.3 Billion Addresses
A network is the first number, or octet, in an IP address
	Network 24 would be 24.0.0.0, etc.
IP addresses are actually written in binary but display as decimal numbers to be a lot easier to read, so they actually look like
	12345678.12345678.12345678.12345678 (Binary is only 1s and 0s but I made it 1-8 so it's easier to read)
A subnet mask simply tells the network which part of the address is the network address, and which part is the host address.
	A subnet mask of 255.255.255.0 on the address 192.168.78.45 means that 192.168.78 is the network address, and .45 is the host address.
When you see a network address with a / at the end, this is called the CIDR which defines the subnet mask.