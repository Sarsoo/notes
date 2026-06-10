---
date: 2026-06-10
title: Types
---
_`type`_ '_`string`_'
- Type specification

'_`string`_'::_`type`_
CAST ( '_`string`_' AS _`type`_ )
- Above can be used for specifying or casting

- Type coercion
_`typename`_ ( '_`string`_' )

# Enum
```sql
CREATE TYPE mood AS ENUM ('sad', 'ok', 'happy');
CREATE TABLE person (
    name text,
    current_mood mood
);
INSERT INTO person VALUES ('Moe', 'happy');
SELECT * FROM person WHERE current_mood = 'happy';
 name | current_mood
------+--------------
 Moe  | happy
(1 row)
```

# Geometric
- point
	- $(x, y)$
- line
	- $Ax+By+C=0$
- lseg
	- $(x_1,y_1)$ to $(x_2,y_2)$
- box
	- Opposite corners
	- $(x_1,y_1)$, $(x_2,y_2)$
- path
	- Open or Closed
	- $(x_1,y_1),(x_2,y_2),...,(x_n,y_n)$
- polygon
	- Similar to closed path, includes area within
	- $(x_1,y_1),(x_2,y_2),...,(x_n,y_n)$
- circle
	- $(x_1,y_1,r)$

# Bit String
- Bit mask

# Text Search 
## `tsvector`
`un-normalised`
```sql
SELECT 'a fat cat sat on a mat and ate a fat rat'::tsvector;
                      tsvector
----------------------------------------------------
 'a' 'and' 'ate' 'cat' 'fat' 'mat' 'on' 'rat' 'sat'
```

- With quotes:
```sql
SELECT $$the lexeme '    ' contains spaces$$::tsvector;
                 tsvector
-------------------------------------------
 '    ' 'contains' 'lexeme' 'spaces' 'the'
```

- Quotes need doubling:
```sql
SELECT $$the lexeme 'Joe''s' contains a quote$$::tsvector;
                    tsvector
------------------------------------------------
 'Joe''s' 'a' 'contains' 'lexeme' 'quote' 'the'
```

- Weighting (titles vs bodies):
	- `A` through `D`
```sql
SELECT 'a:1A fat:2B,4C cat:5D'::tsvector;
          tsvector
----------------------------
 'a':1A 'cat':5 'fat':2B,4C
```

### `to_tsvector`
`normalising`
```sql
SELECT to_tsvector('english', 'The Fat Rats');
   to_tsvector
-----------------
 'fat':2 'rat':3
```

## `tsquery`
```sql
SELECT 'fat & rat'::tsquery;
    tsquery
---------------
 'fat' & 'rat'

SELECT 'fat & (rat | cat)'::tsquery;
          tsquery
---------------------------
 'fat' & ( 'rat' | 'cat' )

SELECT 'fat & rat & ! cat'::tsquery;
        tsquery
------------------------
 'fat' & 'rat' & !'cat'
```
- `&`, `|`, `!`
- `<->` (FOLLOWED BY)
	- `<N>`

### `to_tsquery`
```sql
SELECT to_tsquery('Fat:ab & Cats');
    to_tsquery
------------------
 'fat':AB & 'cat'
```

### Weighting
```sql
SELECT 'fat:ab & cat'::tsquery;
    tsquery
------------------
 'fat':AB & 'cat'
```

### Prefix Matching
```sql
SELECT 'super:*'::tsquery;
  tsquery
-----------
 'super':*
```

# XML
- Syntax checking
- Some type-safe operations
```sql
XMLPARSE ( { DOCUMENT | CONTENT } `value`)

xml '<foo>bar</foo>'

'<foo>bar</foo>'::xml
```

- `xml` -> obj
```sql
XMLSERIALIZE ( { DOCUMENT | CONTENT } `value` AS `type` [ [ NO ] INDENT ] )
```

# [JSON](JSON.md)

# Arrays
```sql
CREATE TABLE sal_emp (
    name            text,
    pay_by_quarter  integer[],
    schedule        text[][]
);
```
- Variable length

```sql
CREATE TABLE tictactoe (
    squares   integer[3][3]
);
```
- Fixed lengths
## Literals
```sql
'{ `val1` `delim` `val2` `delim` ... }'
'{{1,2,3},{4,5,6},{7,8,9}}'

INSERT INTO sal_emp
    VALUES ('Bill',
    '{10000, 10000, 10000, 10000}',
    '{{"meeting", "lunch"}, {"training", "presentation"}}');

INSERT INTO sal_emp
    VALUES ('Carol',
    '{20000, 25000, 25000, 25000}',
    '{{"breakfast", "consulting"}, {"meeting", "lunch"}}');
```

# Composite
- Can be used as columns
```sql
CREATE TYPE complex AS (
    r       double precision,
    i       double precision
);

CREATE TYPE inventory_item AS (
    name            text,
    supplier_id     integer,
    price           numeric
);
```

```sql
CREATE TABLE on_hand (
    item      inventory_item,
    count     integer
);

INSERT INTO on_hand VALUES (ROW('fuzzy dice', 42, 1.99), 1000);
```
