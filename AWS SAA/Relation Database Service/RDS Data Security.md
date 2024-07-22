Data in transit is encrypted by TLS
Data at rest, EBS, is encrypted by KMS
	Storage, logs, snaps and replicas are encrypted
	Encryption cannot be disabled/removed when enabled/added
IAM user/role has a policy that is mapped to a database user
	User/role can generate a token to use as a way to authenticate as that mapped database user