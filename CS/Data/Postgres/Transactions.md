---
date: 2026-06-10
title: Transactions
tags:
  - data/sql/pg
---
- [ ] ```sql
BEGIN;
-- transaction content
COMMIT;
```

```sql
BEGIN;
-- transaction to be rolled back
ROLLBACK;
-- unreachable
COMMIT;
```

# Savepoints
```sql
BEGIN;
SAVEPOINT savepoint_1;
ROLLBACK TO savepoint_1;
COMMIT;
```