---
title: Datasets
tags:
  - infra/zfs
---
# Dataset
- Primary data management unit
- Filesystem or volume
- Features
	- [Compression](Features/_index.md)
	- [Deduplication](Features/_index.md)
	- [Snapshots](Features/Snapshots.md)
## Filesystem
- Can be nested
- `zfs rename x/y/z x/w/z`
- Inheritance
```bash
zfs set compression=lz4 food/vegetables
zfs get compression -r food
NAME                      PROPERTY     VALUE           SOURCE
food                      compression  off             default
food/fruit                compression  off             default
food/fruit/apples         compression  off             default
food/fruit/bananas        compression  off             default
food/fruit/oranges        compression  off             default
food/vegetables           compression  lz4             local
food/vegetables/broccoli  compression  lz4             inherited from food/vegetables
food/vegetables/carrots   compression  lz4             inherited from food/vegetables
food/vegetables/celery    compression  lz4             inherited from food/vegetables
food/vegetables/tomatoes  compression  lz4             inherited from food/vegetables
```
- Mountpoint
```bash
zfs set mountpoint=/path/to/the/new/mountpoint the/dataset/name
```
- Custom [User Properties](https://openzfs.github.io/openzfs-docs/man/master/7/zfsprops.7.html#User_Properties)
```bash
zfs set custom:color=red food/fruit/apples
zfs get custom:color food/fruit/apples
NAME               PROPERTY      VALUE         SOURCE
food/fruit/apples  custom:color  red           local```

## Volume (ZVOL)
- Block device
	- Virtual machines
	- Databases