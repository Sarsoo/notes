---
title: Send+Receive
tags:
  - infra/zfs
---
# Receive from Offsite
```bash
# restore from remove
ssh remotesystem sudo zfs send remotepool/mydataset@snapshotname | sudo zfs receive mypool/mydataset
```

# Send Offsite

```bash
# remote replication
sudo zfs send mypool/mydataset@snapshotname | ssh remotesystem sudo zfs receive remotepool/mydataset
```

```bash
# incremental replication
sudo zfs send -i mypool/mydataset@previous_snapshot mypool/mydataset@latest_snapshot | ssh remotesystem sudo zfs receive remotepool/mydataset
```

## Local Recovery
```bash
# offsite backup
sudo zfs receive mypool/mydataset < /media/usbdrive/backupfile
```

- **Scrub after receive**