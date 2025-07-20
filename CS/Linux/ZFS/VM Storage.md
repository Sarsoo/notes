---
title: VM Storage
---
[ZVOL vs QCOW2 with KVM](https://jrs-s.net/2018/03/13/zvol-vs-qcow2-with-kvm/)

```bash
# Share a ZFS dataset over NFS
sudo zfs set sharenfs=on mypool/vmstorage
```

```bash
# Take a snapshot of a VM storage dataset
sudo zfs snapshot mypool/vmstorage@vmbackup
```

```bash
# Create a clone of a VM base image
sudo zfs clone mypool/vmstorage@vmbackup mypool/vmclone
```

```bash
# Create a 50GB ZVOL for KVM VM
sudo zfs create -V 50G mypool/kvmvol
```
- Thin provisioned
	- Whole 50G not held at once
# Snapshotting

```bash
# Take a snapshot of a ZVOL
sudo zfs snapshot mypool/kvmvol@preupdate
```

```bash
# Rollback to the snapshot
sudo zfs rollback mypool/kvmvol@preupdate
```