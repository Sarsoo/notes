---
title: SLOG
tags:
  - infra/zfs
---
`speed up writes`
- For synchronous writes
	- Databases
- Puts ZIL on separate device
	- ZFS Intent Log

```bash
# Add a SLOG device for improved synchronous write performance
sudo zpool add mypool log /dev/nvme1n1
```
