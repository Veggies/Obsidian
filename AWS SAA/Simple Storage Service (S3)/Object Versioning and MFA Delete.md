Object Versioning
	Disabled by default
		Once enable, cannot ever be disabled
			Enabled bucket can be suspended, then re-enabled
	When disabled, the objects within the buckets are simply replaced.
		When enabled, it creates a backup of the object being replaced
	Key=Name of object
	id=null when versioning is disabled
		id is assigned when versioning is enabled
		id does not change for any objects, replacement objects generate a new id, the replaced object retains it's original id
			Versions can be individually accessed by specifying id
	Delete marker is added when the object is "deleted"
		It's not actually deleted, it's just marked as deleted, which can be undone
		You can version delete and actually delete the object by referencing it's id
			When you delete the latest version of an object, the next latest version will take its place
MFA delete
	Enabled in versioning configuration
	MFA is required to change bucket versioning state
	MFA is required to delete versions