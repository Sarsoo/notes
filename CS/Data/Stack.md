---
title: Stack
tags:
  - data
---
[The Modern Data Stack: Open-source edition](https://www.datafold.com/blog/the-modern-data-stack-open-source-edition)

1. Collection & Integration: 
	- Getting data in the data warehouse/lake for further processing some text
    1. Event Processing: Collecting events and getting them in the warehouse
    2. Data Integration: Adding data from various sources into the warehouse and vice-versa (Reverse ETL)
	    - **Airbyte**
2. [Data Lake](Data%20Lake.md) 
	- Storing, processing, and serving data in a lake architecture, along with its 
		- Storage
			- **Object Storage**
		- File
			- **Parquet**
		- Metadata
			- **[Apache](Apache.md) Iceberg**
		- Compute layers
			- In-process
				- **DuckDB**
				- **Pandas**
				- **Polars**
			- Distributed
				- **Trino**
			- ML & Specialised
				- **[Apache](Apache.md) Spark**
					- Swiss army knife, can handle **Trino** but typically use both
						- **Spark** has lower latency
3. Data Warehousing 
	- Similar to a [data lake](Data%20Lake.md) but an all-in-one solution with all the layers more tightly integrated.
	- **Clickhouse**
		- Distributed
		- PBs of data
	- **Hydra**
		- Single node
		- PostgreSQL extension #sql 
		- Hundreds of GBs
4. Streaming & Realtime 
	- Emerging category for low-latency or operational use cases
	- Use cases
		1. Collecting data (e.g., events) and ingesting it into a data warehouse/lake
		2. Processing data in-flight for enrichment before loading into the long-term storage
		3. Real-time analytics and machine learning, e.g. fraud detection, operational analysis, etc. – where latency matters.
	- **Kafka**
	- Transformations & Compute
		- **[Apache](Apache.md) Spark**
		- **[Apache](Apache.md) Flink**
		- **Materialize**
		- ***Beam?***
			- Format for writing batching or streaming transformations
			- For running on other runners (**Spark**/**Flink**)
			- API for Google DataFlow
5. Data Orchestration 
	- Managing how data pipelines are defined, structured, and orchestrated.
	- SQL Centric #sql 
		- **dbt**
	- All-rounder
		- **[Apache](Apache.md) Airflow**
			- Legacy
		- **Dagster**
			- Resulting product focus
		- **Prefect**
			- Modern Airflow
6. Data Catalogs
	- Finding the right data asset for the problem
	- **Amundsen**
	- **DataHub**
7. BI & Data Apps
	- The consumption layer of the data stack with subcategories, including Notebooks, Self-serve, Dashboards, Code-first Data Apps, and Product/Web Analytics.
	- Self-Serve & Dashboards (Tableu-Like)
		- **Metabase**
		- **Lightdash**
		- **Superset**
	- Notebooks
		- **Jupyter** #py
	- End-to-end Product Analytics
		- **PostHog**
		- **Plausible**

![](https://cdn.prod.website-files.com/66e408a2a1c53743a642f485/67101bf333d764a6c52eeeef_67101bab9357f3a07ea665b9_os-mds-overview.png)

