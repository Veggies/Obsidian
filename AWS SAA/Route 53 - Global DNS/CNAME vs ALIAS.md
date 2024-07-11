A record
	Maps NAME to IP Address
	my.com > 1.24.51.5
CNAME maps NAME to another NAME
	www.my.com > my.com
	**Cannot** map naked/apex name in cname, my.com in this example
ALIAS maps NAME to AWS resource
	**Can** be used for naked/apex (my.com) and normal records (www.my.com)
	ALIAS requests are free when pointing to AWS resources
	ALIAS record type (A, AAAA, etc.) should match what record type the AWS service is pointing to
