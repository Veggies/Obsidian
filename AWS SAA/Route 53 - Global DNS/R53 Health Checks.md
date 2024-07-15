Health checks exist outside of records, but are used by records
Health checkers are located globally
Health checkers run every 30 seconds
Can check TCP, HTTP(S), and HTTP(S) with string matching
Target status can be either healthy or unhealthy
3 types of checks:
	Endpoint checks
		IP or domain endpoint
	Cloudwatch Alarm checks
		Healthcheck status is based on state of cloudwatch alarm
	Health checks on other health checks called checks of checks
If 18% of health checkers report healthy, the health check is healthy