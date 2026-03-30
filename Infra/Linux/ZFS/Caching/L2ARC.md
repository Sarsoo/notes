---
title: L2ARC
tags:
  - infra/zfs
---
`speed up reads`
- Second layer of read caching
	- After [ARC](ARC.md)
- Quick device like SSD for more caching of read-heavy stuff

```bash
# Add an L2ARC device to a pool
sudo zpool add mypool cache /dev/nvme0n1
```