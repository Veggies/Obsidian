- Persistence, use EBS
- Resilience, use EBS
- Storage isolated from an instance's life cycle, use EBS
- Super high performance, use Instance Store
- Cost concern, use Instance store

- Cheap, use ST1 or SC1
- Throughput or streaming, use ST1
- Boot, not ST1 or SC1

- IO1/2 up to 64,000 IOPS
	- Block express up to 256,000 IOPS
- GP2/3 up to 16,000 IOPS
- RAID0 + EBS up to 260,000 IOPS
	- Combined performance of all individual volumes
- More than 260,000 IOPS and tolerate temporary storage, use instance store
