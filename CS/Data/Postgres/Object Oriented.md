---
date: 2026-06-10
title: Object Oriented
---
```sql
CREATE TABLE cities (
  name       text,
  population real,
  elevation  int     -- (in ft)
);

CREATE TABLE capitals (
  state      char(2) UNIQUE NOT NULL
) INHERITS (cities);
```

- Queries all cities including captials
```sql
SELECT name, elevation
  FROM cities
  WHERE elevation > 500;
```

- To exclude captials
```sql
SELECT name, elevation
    FROM ONLY cities
    WHERE elevation > 500;
```