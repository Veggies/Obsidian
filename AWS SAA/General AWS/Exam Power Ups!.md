- Identity Policy vs Resource Policy
	- Identity
		- When controlling multiple different resources across an AWS account
		- A preference for managing permissions all in one place, use IAM
		- Only using one account, since you are only controlling internal users
	- Resource
		- Controlling a single resource
		- Anonymous or Cross-Account
Presigned URLs
	You can create a URL for an object you have no access to
		The URL also has no access to the object
	When you use the URL, the permissions you have access to match the identity the generated it
		If you can't access the object through the URL, this means the identity that generated that object either never had access to object, or it doesn't have access anymore
	Don't generate URLs with role because the temporary role credentials will expire before the URL does