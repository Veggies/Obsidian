- 0.0.0.0 > 255.255.255.255 = ~4.3 Billion Addresses
- A network is the first number, or octet, in an IP address
	- Network 24 would be 24.0.0.0, etc.
- IP addresses are actually written in binary but display as decimal numbers to be a lot easier to read, so they actually look like
	- 12345678.12345678.12345678.12345678 (Binary is only 1s and 0s but I made it 1-8 so it's easier to read)
- A subnet mask simply tells the network which part of the address is the network address, and which part is the host address.
	- A subnet mask of 255.255.255.0 on the address 192.168.78.45 means that 192.168.78 is the network address, and .45 is the host address.
- When you see a network address with a / at the end, this is called the CIDR which defines the subnet mask.

- The CIDR Suffix (The /#) represent all the 1s that belong to the network address. So a CIDR suffix of 20 means there's going to be 20 1s before the host address. 11111111.11111111.11110000.0000 would be the subnet mask of that CIDR of /20. Going back to binary, this means the subnet mask is 255.255.240.0, meaning the host address can range anywhere from 255.255.240.x - 255.255.255.x .