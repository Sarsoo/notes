---
title: ARC
tags:
  - infra/zfs
---
`speed up reads`
- Adaptive Replacement Cache
- Stores frequently read data in RAM

```bash
# Example of setting the ARC size to 32GB on Linux
sudo echo "options zfs zfs_arc_max=34359738368" >> /etc/modprobe.d/zfs.conf
```