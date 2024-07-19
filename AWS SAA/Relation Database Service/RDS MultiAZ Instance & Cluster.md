Multi-AZ Instance
	Only ONE standby replica
	Can't be used for reads or writes, only used for failover events
	Must be in same region
	Standby creates backup and then replicates them across S3 AZs
	Synchronous Replication
		Data is written to the primary RDS, and then immediately copied to the standby RDS
		This is when writes are considered comitted
Multi-AZ Cluster
	ONE writer writes (Synchronous replication) to TWO readers
	Readers/Writer can be used for reading/reading and writing
	Cluster endpoint points at the writer
	Writes are committed when 1 reader has confirmed the write