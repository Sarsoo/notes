```bash
find . -name "*.tf" \! -path "*.terraform*" -type f -printf "%h\n" | sort -u
```