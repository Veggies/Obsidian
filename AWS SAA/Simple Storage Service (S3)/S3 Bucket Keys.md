KMS key is used to create a time limited bucket key within S3 that can be used to generate DEKs within the bucket
	This prevent the throttling and cost issue associated with only using KMS
CloudTrail logs will show the bucket ARN instead of the KMS object when this is enabled
When an object is replicated it will maintain the original object encryption
If replicating plain text to a bucket that has bucket keys enabled, the object is encrypted at the destination