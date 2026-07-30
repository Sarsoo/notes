---
date: 2026-06-27
title: Bash
tags:
  - dev/scripting
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

# piping
```bash
$ more sample_five.sh
#!/bin/bash
function getInput() {
    if test -n "$1"; then
        echo "Read from positional argument $1";
    elif test ! -t 0; then
        echo "Read from stdin if file descriptor /dev/stdin is open"
        cat > file4.txt
    else
        echo "No standard input."
    fi
}
getInput
```