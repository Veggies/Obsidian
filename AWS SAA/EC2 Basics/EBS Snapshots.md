- Snapshots are stored on S3
- Incremental snapshots
	- First snapshot is a full copy of data
	- All sequential snapshots are modifications or additional data, just the differences between the snapshots
- Volumes can be created from snapshots
- Snapshots can be copied from one region to another
- Snaps restore lazily
	- Data is restored/fetched gradually
	- Force a read all data to restore all data immediately
- Fast Snapshot Restore FSR
	- Up to 50 FSR snaps per region, set on Snapshot and AZ
- Billed gigabyte/month
	- Used/stored data, not allocated data