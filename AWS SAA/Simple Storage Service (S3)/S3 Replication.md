- Cross-Region Replication (CRR)
	- From source bucket to one or more destination buckets different regions
- Same-Region Replication (SRR)
	- From source bucket to destination in same region
- SRR and CRR support same and different account replication
- Replication configuration is applied to the source bucket
	- Specifies
		- Destination bucket
		- IAM role to use for replication process
			- Configured to allow S3 to assume it
			- Gives permissions to read source, and replicate on destination
	- When replicating in the same AWS account
		- Both buckets trust IAM
			- Both trust roles
			- Automatically has access to the source and destination as long as the roles permission policy grants that access
	- When replicating to a different AWS account
		- Source account and role is not automatically trusted
		- Destination bucket policy must define that a role in a separate account can write or replicate objects into the bucket
- Replication options
	- Replicate either entire bucket or subset
		- Subset is a rule that filters objects by prefix or tags or a combination of both
	- Can choose what storage class the replicated objects will be placed into
	- Define ownership
		- Default is the source account
	- Replication Time Control (RTC)
		- Guaranteed 15 minute replication SLA
- S3 Replication Considerations
	- By default replication is not retroactive
		- Versioning must be turned on to enable replication (On both source and destination buckets)
		- Batch replication can be used to replicate pre-existing objects prior to turning on replication
	- One-way replication by default, source to destination only
		- Bi-directional is an additional setting
	- Capable of handling unencrypted objects
	- Capable of handling encrypted objects with SSE-3, SSE-KMS (with extra config), SSE-C
	- Source bucket owner needs permissions on objects that are being replicated
		- Source account must own the objects
	- Will not replicate system events (IE changes by life cycle management), glacier or glacier deep archive
	- Deletes are not replicated (DeleteMarker items, but can be configured)
- Replication Use Cases
	- SRR
		- Log Aggregation (Centralized logging)
		- Create synchronization between accounts
		- Resilience with strict sovereignty
	- CRR
		- Global resilience improvements
		- Latency reduction