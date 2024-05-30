Grants or Denies access to AWS Products/Features to any Identity that uses that policy
	An identity policy is basically just a set of permissions.
	Policies from groups, or inline, or managed, can all be assigned and work together. IE, Sally can be a group member of Dev and Ops, have their own inline policy, and be attached to a manage policy. All the policies will operate together under the principle of Deny Allow Deny.

Statements
	- Statements start with an SID, a statement id. It just gives a description of what the statement is doing.
	- The action format is service:operation(s), wild cards are supported.
		- The action is what is either being allowed or denied. IE access to resources.
	- Effect is either Allow, or Deny.
		- Denies will always trump Allows
		- Implicit deny takes effect if there is no explicit allow. Basically, if it isn't allowed, then it's automatically denied. This goes across all policies applied to the identity.

Policy types:
	- Inline policy is when a policy is attached to an individual identity
	- Managed policy can be applied to multiple individuals. This is basically a group policy.
		- Both AWS managed policies and customer managed policies.
