---
title: Virtualisation
tags:
  - infra/virtualisation
---

# [libvirt](https://libvirt.org/docs.html)
- `virsh`
	- `list`
		- Show (running) VMs
	- `edit`
		- Edit XML config
	- `dumpxml`
		- Get config as XML
	- `domifaddr`
		- IPs associated to virtual interfaces
	- `net-edit`
		- Live update net config
- `libvirtd`
	- Main server daemon
	- `sudo systemctl start libvirtd && sudo systemctl enable libvirtd`

```
qemu:///session                      (local access to per-user instance)
qemu+unix:///session                 (local access to per-user instance)

qemu:///system                       (local access to system instance)
qemu+unix:///system                  (local access to system instance)
qemu://example.com/system            (remote access, TLS/x509)
qemu+tcp://example.com/system        (remote access, SASl/Kerberos)
qemu+ssh://root@example.com/system   (remote access, SSH tunnelled)
```

| Connection      | Config Location                    |
| --------------- | ---------------------------------- |
| qemu:///system  | /etc/libvirt/qemu.conf             |
| qemu:///session | $XDG_CONFIG_HOME/libvirt/qemu.conf |
| qemu:///embed   | $rootdir/etc/qemu.conf             |

# [kvm](https://linux-kvm.org/page/Main_Page)

# [qemu](https://wiki.qemu.org/Main_Page)
