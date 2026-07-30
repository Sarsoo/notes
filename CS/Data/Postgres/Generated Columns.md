---
date: 2026-06-10
title: Generated Columns
tags:
  - data/sql/pg
---
```sql
CREATE TABLE people (
    ...,
    height_cm numeric,
    height_in numeric GENERATED ALWAYS AS (height_cm / 2.54)
);
```

```sql
CREATE TABLE people (
    ...,
    height_cm numeric,
    height_in numeric GENERATED ALWAYS AS (height_cm / 2.54) [STORED or VIRTUAL]
);
```

