---
date: 2026-06-13
title: Proxmox and FreeIPA
tags:
  - infra/linux
  - infra/virtualisation
---
`- FreeIPA picks massive IDs
- Default `/etc/subuid`/`/etc/subgid` doesn't include these ranges
```
root:100000:65536
```
- Default lxc mappings doing include these ranges back either

```
root:100000:65536
aj:165536:65536
baccie:231072:65536
root:712600000:200001 <----
```
- Allow root to map the ranges
```hcl
// default uid range
  idmap {
    type         = "uid"
    container_id = 0
    host_id      = 100000
    size         = 65535
  }

// default gid range
  idmap {
    type         = "gid"
    container_id = 0
    host_id      = 100000
    size         = 65535
  }

// add ipa ranges
  idmap {
    type         = "uid"
    container_id = 712600000
    host_id      = 712600000
    size         = 200000
  }

  idmap {
    type         = "gid"
    container_id = 712600000
    host_id      = 712600000
    size         = 200000
  }
```



# Samba

- ipa-client-samba
	- https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1012592
	- `groupadd nobody`