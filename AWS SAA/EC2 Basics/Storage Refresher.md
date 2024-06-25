Direct (Local) storage - Storage on the EC2 host
Network Attached Storage - Volumes delivered over network (Elastic Block Store)
Ephemeral Storage - Temporary storage
Persistent storage - Permanent storage, lives on past the lifetime of the EC2 instance

Block Storage - Volume containing a collection of addressable blocks
	No structure provided. An HDD, SSD, etc.
	Bootable and Mountable
File Storage - File share with structure
	Not bootable, but is mountable
Object Storage - collection of objects, like S3
	Not bootable or mountable

IO (block) size
IOPS
	Reads/Writes per second
Throughput
	IO * IOPS = Throughput