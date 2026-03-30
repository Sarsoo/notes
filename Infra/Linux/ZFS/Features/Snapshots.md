---
title: Snapshots
tags:
  - infra/zfs
---
[ZFS clones: Probably not what you really want](https://jrs-s.net/2017/03/15/zfs-clones-probably-not-what-you-really-want/)

```bash
sudo zfs rollback mypool/mydataset@snapshotname
```

```bash
sudo zfs list -t snapshot
```

# Block files

```bash
sudo zfs send poolname/setname@0 | pv > /coldstorage/setname@0.zfsfull
 108MB 0:00:00 [ 297MB/s] [<=>]

ls -lh /coldstorage
total 1.8M
-rw-r--r-- 1 root root 108M Sep 15 16:26 setname@0.zfsfull
```

```bash
sudo zfs send -i poolname/setname@0 poolname/setname@1 | pv > /coldstorage/setname@0-@1.zfsinc
 108MB 0:00:00 [ 316MB/s] [<=>]
 
sudo zfs send -i poolname/setname@1 poolname/setname@2 | pv > /coldstorage/setname@1-@2.zfsinc
 108MB 0:00:00 [ 299MB/s] [<=>]
 
ls -lh /coldstorage
total 5.2M
-rw-r--r-- 1 root root 108M Sep 15 16:33 setname@0-@1.zfsinc
-rw-r--r-- 1 root root 108M Sep 15 16:26 setname@0.zfsfull
-rw-r--r-- 1 root root 108M Sep 15 16:33 setname@1-@2.zfsinc
```