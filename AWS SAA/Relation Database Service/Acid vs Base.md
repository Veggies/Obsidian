CAP Theorem
	Consistency
		Latest data, or error
	Availability
		No errors
	Partition Tolerant
ACID - Consistency, SQL
	Atomic
		All or none of transaction succeeds or fails
	Consistent
		Move one valid state to another
	Isolated
		No transactions interact or interfere with each other
	Durable
		Once transaction complete the data will not be susceptible to failure by any means.
	ACID references to RDS and limits scaling
Base - Availability, NoSQL
	Basically Available
		Read and write are available as much as possible
		No consistency guarantees
	Soft State
		Database doesn't enforce consistency, application/user is responsible
	Eventually Consistent
		Reads will eventually be consistent
	Highly scalable and high performance
	DynamoDB