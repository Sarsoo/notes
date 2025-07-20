---
title: ACLs
---
- Standard UNIX perms
```bash
sudo chmod 700 /mypool/mydataset
sudo chown user:group /mypool/mydataset
```

# ACLs
```bash
# for "username"
sudo setfacl -m u:username:rwx /mypool/mydataset
```

## Delegation
- Specific perms delegated to non-privileged users
	- Create snapshots/mount datasets

```bash
# for "user"
sudo zfs allow user create,snapshot mypool/mydataset
```

```bash
# view perms
sudo zfs allow mypool/mydataset
```

```bash
# remove perms for "user"
sudo zfs unallow user create,snapshot mypool/mydataset
```