---
title: Monitoring
tags:
  - infra/zfs
  - devops/observability
---
# Status

```bash
sudo zpool status mypool
  pool: mypool
 state: ONLINE
  scan: resilvered 2.10G in 0h3m with 0 errors on Sun Sep  5 12:49:01 2024
config:

        NAME        STATE     READ WRITE CKSUM
        mypool      ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            ada1    ONLINE       0     0     0
            ada3    ONLINE       0     0     0

errors: No known data errors

# space usage etc
sudo zpool list mypool
```

# I/O

```bash
# Monitor I/O performance
sudo zpool iostat -v 5
```

## History

```bash
sudo zpool history mypool
History for 'mypool':
2024-11-05.14:45:32 zpool create mypool mirror /dev/ada1 /dev/ada2
2024-11-05.15:10:45 zpool add mypool /dev/ada3
2024-11-05.15:22:13 zfs create mypool/dataset1
2024-11-05.15:55:01 zfs set compression=on mypool/dataset1
```

```bash
# -i includes internal events
sudo zpool history -i mypool
History for 'mypool':
2024-11-05.14:45:32 zpool create mypool mirror /dev/ada1 /dev/ada2
2024-11-05.15:10:45 zpool add mypool /dev/ada3
2024-11-05.15:55:01 zfs set compression=on mypool/dataset1
2024-11-06.09:10:21 scrub initiated
2024-11-06.09:50:42 scrub completed
```
