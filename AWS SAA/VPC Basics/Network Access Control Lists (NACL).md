NACLs filter traffic coming into (Inbound) the subnet, or out of the (Outbound) subnet, not within the same subnet
	Cannot be attached to resources, only to subnets
	Cannot define resources, only IPs/CIDR, Port/Ranges, and protocols
NACLs allow explicit allows and explicit denies
NACLs are stateless
NACLs must have a rule number defined to each rule
	Rules match the destination/source IP range, port range, and protocol
	NACLs are processed in order starting with the lowest rule number
	Once a match occurs with the traffic, the search stops and the rule is applied
		If nothing matches, it is denied.
Default NACL for VPC
	Allow ALL rule (Rule 110)
	Implicit Deny (Rule , * occurs after allow all)
Custom NACL
	Starts with implicit deny
Each subnet can have one NACL (Consisting of many rules)
	One NACL can be associated with many subnets