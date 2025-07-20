---
title: ZPOOL
---
# Storage Pool (ZPOOL)
- One or more [VDEV](VDEV.md)

## Adding
```bash
sudo zpool add mypool /dev/ada3
```
- *This increases the storage capacity of the pool by adding `/dev/ada3`. It is important to note that adding devices to a pool is a permanent operation. Devices added to the pool cannot be removed unless specific configurations, such as mirrored VDEVs, are used.*

## Replacing
- Can increase capacity
```bash
# after physically replacing failed device
sudo zpool replace mypool /dev/ada1 /dev/ada4
```

## Removing
- Depends on the architecture
```bash
sudo zpool remove mypool /dev/ada3
sudo zpool status mypool
  pool: mypool
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        mypool      ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            ada1    ONLINE       0     0     0
            ada2    ONLINE       0     0     0

errors: No known data errors
```

## Status
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

## Scrub
- Check data integrity
- **Do periodically**
	- Every few weeks for active datasets
```bash
sudo zpool scrub mypool
```

## Clearing Errors
- After transient failure
```bash
sudo zpool clear mypool /dev/ada2
```

## Destroy
```bash
sudo zpool destroy new-pool
```

# Export
- Detach from running system

```bash
sudo zpool export mypool
```

## Import

```bash
sudo zpool import
   pool: mypool
     id: 1234567890123456789
  state: ONLINE
 action: The pool can be imported using its name or numeric identifier.
 config:

        mypool     ONLINE
          mirror-0  ONLINE
            ada1    ONLINE
            ada2    ONLINE
```

```bash
sudo zpool import mypool
sudo zpool status
  pool: mypool
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        mypool      ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            ada1    ONLINE       0     0     0
            ada2    ONLINE       0     0     0

errors: No known data errors
```