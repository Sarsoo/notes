---
title: ZFS
---
[OpenZFS](https://openzfs.org/wiki/Main_Page)

# Tools
[ZFS Capacity Calculator](https://wintelguy.com/zfs-calc.pl)
[ZFSBootMenu](https://docs.zfsbootmenu.org/en/latest/index.html)

# RAID Equivalents
- `RAID 0`
	- Stripe across disks without parity
	- 100% utilisation
- `RAID 1`
	- Mirror
	- 50% utilisation (for 2 way mirror, $\frac{1}{n}$ in general)
- `RAID 5`
	- Stripe across disks with parity 1
	- $1-\frac{1}{n}$ utilisation (67% for 3 disks, 80% for 5)
- `RAID 6`
	- Stripes across disk with parity 2
	- $1-\frac{2}{n}$ utilisation (60% for 5 disks)
- `RAID 10`
	- Stripe across mirrors
	- 50% utilisation (for 2 way mirror, $\frac{1}{n}$ in general)

# Guides
[ZFS: You should use mirror vdevs, not RAIDZ.](https://jrs-s.net/2015/02/06/zfs-you-should-use-mirror-vdevs-not-raidz/)
- Use mirrored pairs of devs as vdevs instead of RAIDZ
	- Quicker re-silver
	- Very little impact on performance of pool
	- Survival chances
		- $1-(\frac{f}{n-f})$
		- $f$ = number of disks already failed
		- $n$ = number of disks in full pool
		- e.g 8 disk pool (2-way mirrors)
			- 100% survival of the first disk failure
			- 85.7% survival of a second disk failure
			- 66.7% survival of a third disk failure
- *don’t be greedy. 50% storage efficiency is plenty.*
- *for a given number of disks, a pool of mirrors will significantly outperform a RAIDZ stripe.*
- *a degraded pool of mirrors will **severely** outperform a degraded RAIDZ stripe.*
[ZFS Handbook](https://www.zfshandbook.com)
[ZFS write allocation in 0.7.x](https://jrs-s.net/2018/08/24/zfs-write-allocation-in-0-7-x/)
- Don't mix rust and SSD in the same pool or vdev
[Assessing the Potential for Data Loss](https://www.truenas.com/community/resources/assessing-the-potential-for-data-loss.227/)
- 

# Install

```bash
# debian
sudo apt install zfsutils-linux
# fedora
sudo dnf install https://zfsonlinux.org/epel/zfs-release.el7_9.noarch.rpm
sudo dnf install zfs
sudo modprobe zfs
# arch
sudo yay -S zfs-dkms zfs-utils
sudo modprobe zfs
```

```bash
lsmod | grep zfs
```
# Create

- Check devices
```bash
lsblk
```

- Create [ZPool](ZPool.md)
```bash
# single disk
sudo zpool create mypool /dev/sdb
# mirror
sudo zpool create mypool mirror /dev/sdb /dev/sdc
# raid-z1
sudo zpool create mypool raidz /dev/sdb /dev/sdc /dev/sdd
```

