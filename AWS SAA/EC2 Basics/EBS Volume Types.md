## General Purpose
GP2 volume
	Throughput limited to 250 mb/s
	Small as 1GB, or large as 16TB
	IO Credit
		16 KB
		IOPS assume 16kb/s
			1 IOPS is 1 IO in 1 second
	IO Credit has a capacity of 5.4 million, starts off full
		Fills at baseline performance based on size
			Fills at 100 credits per second at minimum
			3 IO Credits per second per GB of volume size
				Anything below 33.33 GB gets 100 credit minimum
		Can burst 3,000 IOPS
	Volumes larger than 1TB
		Baseline performance equal to or greater than 3,000 IOPS
		Any volumes larger than 5.33 TB achieve 16,000 IOPS
		Does not use credit system
GP3
	Throughput limited to 1,000 MB/s
	3,000 IOPS & 125MiB/s
	1GB-16GB
	Extra cost for up to 16,000 IOPS or 1,000 MiB/s

## Provisions IOPS SSD
io2 block express 1000IOPS/GB (Max)
io1 50IOPS/GB (Max)
io2 500IOPS/GB (Max)
Low latency, IO intesive
