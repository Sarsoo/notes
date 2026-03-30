---
title: Features
tags:
  - infra/zfs
---
# [Encryption](Encryption.md)

# [Snapshots](Snapshots.md)

# [Send+Receive](Send+Receive.md)

# [ACLs](ACLs.md)

# Compression
- Transparent
- Algorithms
	- **`lz4`**
		- High-speed compression with a balance of performance and ratio.
		- *General-purpose workloads, logs, databases, etc.*
	- `lzjb`
		- Older algorithm, predecessor of `lz4`
		- *Legacy systems or backward compatibility.*
	- `zle`
		- Compresses zero-filled blocks.
		- *Virtual machine images and datasets with zero-filled blocks.*
	- `gzip`
		- Offers compression levels from `gzip-1` to `gzip-9`, with varying performance.
		- *Archival data, backups, where storage efficiency is critical.*
	- **`zstd`**
		- Newer algorithm, faster than `gzip` with better ratios.
		- *Suitable for archival data and large files.*

**`lz4` for most stuff, `zstd` for archival**

```bash
sudo zfs set compression=lz4 mypool
```

```bash
zfs get compression,compressratio mypool
```

# Deduplication
- Uses lots of memory
	- Checks entire deduplication table (DDT)
	- ~**5GB** RAM/**1TB** deduplicated data
- Adds complexity
	- Irreversible
	- DDT continues to grow as data added

```bash
sudo zfs set dedup=on mypool
```
