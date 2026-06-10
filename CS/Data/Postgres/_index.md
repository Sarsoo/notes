---
date: 2026-06-10
title: Postgres
---
# Quotes
- `"`
	- Delimited Identifiers
	- Object in psql
	- `SELECT * FROM "customer";`
		- Case-sensitive
	- Can be unquoted
		- `SELECT * FROM customer;`
		- Case-insensitive
- `'`
	- Strings

# DB Management
```bash
createdb mydb
dropdb mydb
```

# PSQL
```
psql mydb
```