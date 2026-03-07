---
title: Find All Folders
tags:
  - devops/iac/terraform
---
```bash
find . -name "*.tf" \! -path "*.terraform*" -type f -printf "%h\n" | sort -u
```