S3 Standard
	Object is replicated across at least 3 availability in the AWS region
	When objects have been stored durably, S3 sends a HTTP/1.1 200 status
	First byte latency, objects uploaded are available within milliseconds
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