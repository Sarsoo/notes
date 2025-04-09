---
title: Data Lake
---
- Store large volumes of data in raw form
- Data processed and used as basis for analytics
- Store all types of data
	- Structured
		- Database tables
		- Excel sheets
	- Semi-structured
		- XML files
		- Webpages
	- Unstructured
		- Images
		- Audio files
- Typically stored in **staged zones**
	- Raw
	- Cleansed
	- Curated
- Use cases
	- Big data analytics
	- Machine learning
	- Predictive analytics
- Workloads
	- Big data processing
	- SQL queries
	- Text mining
	- Streaming analytics
	- Machine learning
- Eliminates silos

# Vs

|             | lake                                                       | warehouse                                                  | lakehouse                                                                                               |
| ----------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| type        | structured, semi-structured, unstructured                  | structured                                                 | structured, semi-structured, unstructured                                                               |
|             | relational, non-relational                                 | relational                                                 | relational, non-relational                                                                              |
| schema      | schema on read                                             | schema on write                                            | schema on read/write                                                                                    |
| format      | raw, unfiltered                                            | processed, vetted                                          | raw, unfiltered, processed, curated, delta format files                                                 |
| sources     | big data, iot, social media, streaming data                | application, business, transactional data, batch reporting | big data, iot, social media, streaming data, application, business, transactional data, batch reporting |
| scalability | easy to scale at low cost                                  | difficult and expensive to scale                           | easy to scale at low cost                                                                               |
| users       | data scientists/engineers                                  | data warehouse professionals, business analysts            | business analysts, data engineers, data scientists                                                      |
| use cases   | machine learning predictive analytics, real-time analytics | core reporting, bi                                         | core reporting, bi, machine learning, predictive analytics                                              |

# Data Lakehouse
- Layers on top of the data lake
	- Delta lake storage layer
	- Handles ACID transactions for data reliability, streaming integrations
		- Data versioning and schema enforcement

# Architectures
- Resource management and orchestration
	- Consistently execute tasks
- Connectors for easy access
	- Workflows to allow users to access and share data in the right form
- Reliable analytics
	- Fast, scalable and distributed
	- Diverse range of workload categories across multiple languages
- Data classification
	- Profiling, cataloging and archiving
	- Track
		- Content, quality, location and history
- Extract, load, transform processes
	- Extracted from multiple sources
	- Loaded into raw zone
	- Cleaned and transformed after extraction
- Security & support
	- Masking
	- Auditing
	- Encryption
	- Access monitoring
- Governance & stewardship
	- Users educated on architecture