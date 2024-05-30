Role is intended to be used for multiple or an uncertain number of principals
	A role is temporary, assumable identity. You are basically becoming another identity, you gain their permissions. It's like a superhero costume, but only temporary.
Roles have two policies:
	Permissions policy
	Trust policy
		Controls which identities can assume the Role, a list of users allowed.
			Can reference identities in the same account (IAM, other Roles, AWS services)
			Can reference identities in OTHER AWS accounts, can allow anonymous usage, and different identities such as Facebook, twitter, and google.
		When a role becomes assumed by an identity, it will generate security credentials for that identity. They are temporary, time limited.
Use cases:
	During break glass situation
	SSO or >5000 identities
		A role can be assigned through SSO or something like an Active Directory
		External accounts cannot be used in AWS directly
	Mobile apps, such as a ride sharing app.
		Use through ID federation
	Cross account access