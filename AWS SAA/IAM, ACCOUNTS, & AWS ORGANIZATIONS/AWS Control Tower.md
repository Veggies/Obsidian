- Control tower
	- Quick and easy setup of multi-account environment
	- Orchestrates other AWS services create this multi-account environment
	- Creator of AWS Control Tower becomes management account of the control tower
- Landing Zone
	- Creates the AWS Organization
			- Automatically creates two OUs
				- Foundational (AKA Security)
					- Creates two AWS accounts
						- Audit
							- SNS & Cloudwatch stored in this account
						- Log Archive
							- AWS Config & CloudTrail stored in this account
				- Custom (Sandbox)
	- Provides SSO/federation and centralized logging + auditing
	- Home region is where the control tower is initially created in
- Guard Rails
	- Detect or mandate rules across accounts
	- Three types
		- Mandatory
			- Always Applied
		- Strongly Recommended
		- Elective
	- Preventive mode stop thing from happening
		- Implemented using SCP
		- Either enforced or disabled
	- Detective mode identify compliance
		- Compliance checks
			- Clear
			- In violation
			- Not enabled
- Account Factory
	- Account Factory created accounts
		- Account factory contains an account and network template for creation of accounts
	- Can be done by cloud admins or end users
		- Includes guardrails automatically
	- Accounts can be closed or repurposed
- Dashboard
	- Single page overview of the environment