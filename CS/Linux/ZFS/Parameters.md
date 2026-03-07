---
title: Parameters
tags:
  - infra/zfs
---
[About ZFS recordsize](https://jrs-s.net/2019/04/03/on-zfs-recordsize/)
[ZFS tuning cheat sheet](https://jrs-s.net/2018/08/17/zfs-tuning-cheat-sheet/)
# `ashift`
- `recommended = 12`
- vdev-scoped
	- Immutable
- Physical (on-disk) sector size
	- ZFS stores data in records
		- Composed of sectors
- Set in bits
	- `ashift=9` = 512B sectors
	- **`ashift=12` = 4K sectors**
	- `ashift=13` = 8K sectors
		- Some newer SSDs
- If you get it wrong, overshoot - don't undershoot

# `recordsize`
- dataset-scoped
	- Mutable
- Defaults to 128K (as of 2019)
	- Pretty reasonable
- Want to map close to workload size in dataset
	- JPGs ~5MB
		- `recordsize=1M`
		- Prevents undue fragmentation
			- Fewer IOPS
	- MySQL InnoDB
		- `recordsize=16K`
		- (InnoDB defaults to 16KB page size)
	- MySQL InnoDB in a VM
		- KVM .qcow2 files default to a `cluster_size` of 64KB
		- `recordsize=64K`
- Too High
	- Increased latency
- Too Low
	- Greater fragmentation
		- Performance issues down the road
	- Limit compression ability
	- ZFS compression is by record
	- `compression=lz4`, `ashift=12`, and `recordsize=4K`
		- No compression
			- Sector size is equal to record size
			- Can't store data in half a sector
		- Default `recordsize=128K`
			- Could easily do 1.7:1
- Torrenting
	- Torrenting access is small chunks with random access
		- Suggests smaller record size
	- Actual access is as larger files
		- Suggests `recordsize=1M`

# `xattr`
- `xattr=sa`
- Sets Linux Extended Attributes directly in inodes instead of as files in hidden folders
- Performance improvement on datasets with lots of files
	- Especially with SELinux
- Little effect on datasets with few large files

# [`compression`](Features/_index.md)
- `compression=lz4`

# `atime`
- `atime=off`
- Don't set access time
- Can double IOPS load
- Who cares