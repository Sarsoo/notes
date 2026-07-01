---
date: 2026-06-27
title: Bash
---
# Join Array
## By Comma
```bash
foo=(a "b" c)
$(IFS=, ; echo "${foo[*]}")
```

## By New Line
```bash
foo=(a "b" c)
printf "%s\n" "${foo[@]}"
```