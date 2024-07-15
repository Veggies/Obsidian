Use Case
	Simple loading balancing
	Testing new software versions
Record weight
	A record weight with 0 is never returned
	Records are assigned a weight value
		Records are returned in comparison to the total weight of all records combined
			As an example, 40, 40, 20. Total is 100. Returns are 40% of the time and 20% of the time. Total CAN be greater than 100!
		An unhealthy record is skipped