Regional & Public Service
	KMS Keys are isolated to the region they are created in, and do not leave.
Create store and manage keys
	Symmetric and Asymmetric
Keys never leave KMS
	Provides FIPS 140-2 (Level 2)
KMS Keys
	Contains ID, date, policy, description and state
	Backed by physical key material
		Can be generated or imported
		Can directly encrypt or decrypt 4kb of data
Keys are never stored in plain text form on disk
Data Encryption Keys (DEKs)
	Generated using KMS keys
		Linked to the KMS key that created it
	Works on data > 4KB
	DEKs is not stored by KMS in anyway. It just provides it to you or the service using KMS, then discards it
		Provides a plaint text key
		Provides a cipher text version of the same key
			Encrypted used the KMS key that generated the DEK
				This allows for you have an encrypted version of the key that can then be sent to KMS to be decrypted, allowing you to have the decrypted plain text version of the DEK
AWS owned or Customer Owned
	AWS keys work in the background and are mostly not interacted with
	Customer owned
		AWS Managed
			Automatically created by AWS when you use a service that integrates with AWS
			Key rotation cannot be disabled, rotates approx. annually
		Customer Managed
			Created explicitly by the customer, more configurable than AWS managed keys
			Key rotation is optional, enabled by default, approx. annually
	Keys contains backing key and previous backing key
		This means that when a rotate occurs, previously encrypted data with the older key can still be decrypted.
Key policy
	Resource policy
	Every key has one