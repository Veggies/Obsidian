Single Put Upload
	One data stream
		If data upload fails at any point, upload must be restarted from scratch
Multipart Upload
	Breaks data up into parts (Like when torrenting, the zip is broke up into many zips)
		Min data size is 100MB for multipart
		Can be split into max. 10,000, parts.
			Each part can be anywhere from 5MB to 5GB
				The last part can be smaller than 5MB if needed
		Each part can fail, but when a part fails, just that part's upload is restarted
Transfer Acceleration
	Must be enabled
	S3 Bucket name:
		Cannot contain periods
		Must be DNS compatible
	Uses best performing nearest edge location
		Transit data being upload over the AWS global network, a network under control of AWS
			Typically a direct link to other AWS network locations