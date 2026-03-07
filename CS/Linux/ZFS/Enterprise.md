---
title: Enterprise
tags:
  - enterprise
---
# HA
- Cluster with failover
- Multiple nodes connected to same storage
	- iSCSI
	- Fibre
	- NAS over NFS
- Pacemaker/Corosync

```bash
# Configure ZFS resource for Pacemaker
sudo pcs resource create zfspool ocf:heartbeat:ZFS pool=myzpool
sudo pcs resource group add zfs_group zfspool
```

```bash
# Incremental replication
sudo zfs send -i mypool@prevsnap mypool@currsnap | ssh backup_node sudo zfs receive remotepool
```

```
+---------------+         +---------------+
|     Node 1    |         |     Node 2    |
|  Active ZFS   |         |  Standby ZFS  |
+---------------+         +---------------+
      |                          |
      |  Pacemaker + Corosync    |
      +--------------------------+
           | Shared Storage |
           +----------------+
                [myzpool]
```