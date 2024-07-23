Proxy has long term connection pool to primary RDS
	Incoming connections connect to proxy
		Instead of applications opening and closing connections, these long term connections are just reused
		Must quicker versus direct connection
Use cases
	Too many connection errors
	AWS Lambda
	Long running applications
Auto scaling and highly available