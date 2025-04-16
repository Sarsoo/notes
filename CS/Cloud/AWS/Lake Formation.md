---
title: Lake Formation
tags:
  - data
  - cloud
---
[Data Lake](../../Data/Data%20Lake.md)
- Govern
- Scale
- Globally share data
- [Glue](Glue.md) Data Catalog
	- Centralise data security & 
- Relational database management system (RDBMS)-like permissions model
	- Grant and revoke access to Data Catalog resources
		1. Metadata-level permissions on the catalog resources
		2. Storage-level access on the underlying [S3](S3.md) storage
- Data in [S3](S3.md)

![](https://docs.aws.amazon.com/images/lake-formation/latest/dg/images/lf-workflow.png)
1. Get metadata
	- Submits query or ETL script to analytical engine
		- [Athena](Athena.md)
		- [Glue](Glue.md)
		- [EMR](EMR.md)
		- Redshift Spectrum

# Components
- [Glue](Glue.md) to orchestrate jobs and crawlers