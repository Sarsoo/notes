---
title: VDEV
---
# Virtual Devices
- Not physical disks
- Logical groupings of
- Backbone of a [ZPool](ZPool.md)
- Can be a single disk
	- Or multiple disks
		- Mirrors
		- RAID-Z
## Striped
`RAID-0`
* Stripes data across all the drives
* No fault tolerance
```bash
sudo zpool create new-pool /dev/sdb /dev/sdc
```

## Mirrored
`RAID-1`
* Survives failure of 1 drive (for mirror of 2 drives)
```bash
sudo zpool create new-pool mirror /dev/sdb /dev/sdc
```
```bash
# -m for mountpoint
sudo zpool create -m /usr/share/pool new-pool mirror /dev/sdb /dev/sdc
```

## RAID-Z
- Data redundancy and protection
- RAID-Z[1/2/3]
	- Levels of parity
	- Disks that can fail
```bash
sudo zpool create myraidzpool raidz1 /dev/ada1 /dev/ada2 /dev/ada3 /dev/ada4
```

# Detach
- Detach a mirrored device
```bash
sudo zpool detach zeepool c2t1d0
```