S3 Standard
	Object is replicated across at least 3 availability in the AWS region
	When objects have been stored durably, S3 sends a HTTP/1.1 200 status
	First byte latency
		Objects uploaded are available within milliseconds
	Use case
		S3 standard should be used for frequently accessed data that is important and non-replaceable
	Costs
		GB/month fee
		$/GB for transfer out
		Price per 1,000 requests
S3 Standard-IA (Infrequent Access)
	 Replicated across 3 AZs, publicly available, first by latency
	 About half of the price of S3 Standard
	 Costs
		 Per GB data retrieval fee
		 Minimum duration charge of 30 days, objects can be stored for less but will be charged at minimum 30 days of storage per object
		 Minimum size charge of 128kb per object
	Use case
		Should be used for long-lived data, but is important and access is infrequent
S3 One Zone IA
	Retrieval fee, 30 day minimum, 128kb minimum charges
	Data is only stored in one availability zone, cheaper storage
	Use case
		Long lived data, non critical, replaceable, and infrequent access

# Part 2
S3 Glacier - Instant
	Like S3 Standard IA, cheaper storage, more retrieval costs
	Stored in 3 AZs in the region
	Costs
		Per GB retrieval fee
		Costs increase with frequency of data access
		Minimum 90 day duration charge
		128kb charge per object
	Use case
		Long lived data that is accessed ~once a quarter
S3 Glacier - Flexible (Chilled state data)
	About 1/6 cost of storage versus standard
	Replicated across 3 AZs
	Accessing objects requires a retrieval process
		When data is retrieved, it is treated as S3 Standard-IA temporarily (Until is no longer be used)
			Expedited 1-5 minutes
			Standard 3-5 hours
			bulk 5-12 hours
			Faster=More expensive
	First byte latency of minutes or hours
	Objects **cannot** be made publicly accessible
	Cost
		40kb minimum billable size
		90 day minimum billable duration
	Use case
		Archival purpose/data
		Frequent/real time access isn't needed
S3 Glacier - Deep Archive (Frozen data)
	The cheapest storage option
	Cost
		40kb minimum
		180 day minimum
	Objects cannot be publicly accessible
		Requires a retrieval process
			Standard 12 hours
			Bulk 48 hours
			First byte latency = hours or days
	Use Case
		Archival that needs to be rarely or never accessed
S3 Intelligent-Tiering
	5 Different Storage Tier
		Frequent Access Like Standard
		Infrequent Access Like Standard IA
			Moved after 30 days
		Archive Instant Access Glacier Instant
			Moved after 90 days
		Archive Access Glacier Flex - Optional
			Moved after 90 - 270 days
		Deep Archive Glacier Deep Archive - Optional
			180 - 730 days
	Monitors usage of objects to place into appropriate tier
	Designed for long-lived data with changing or unknown amounts of use
	Monitoring and automation cost per 1,000 objects, no retrieval charges