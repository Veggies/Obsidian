Any data backed up by RDS is regionally resilient
	Stored in an S3 bucket, but only manageable/visible in RDS
Snapshots are incremental
	Snapshots must be deleted manually
Automatic Backups
	Retain for 0-35 days
	Every 5 minutes transaction logs are created
		Incremental backup checks for changes and then backup
			Backup happen once a day
Restore
	Creates a new RDS instance when restoring