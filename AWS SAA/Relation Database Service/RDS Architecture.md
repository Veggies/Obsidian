Database Server as a Service
	Multiple databases on one server
	No access to OS or SSH
Runs within a VPC
	Primary Instance and standby instances run on separate AZs
RDS instances has dedicated EBS per instance
	Each instance can run more than one DB
	Synchronous replication
		Data is replicated to standby as soon as changes occur
Costs
	Instance Size and Type
	Multi AZ or not
	Storage type and mount
	Data transfer
	Backups and snapshots