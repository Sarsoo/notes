---
title: Encryption
---
# Create an Encrypted Dataset
```bash
# default AES-256-CCM
sudo zfs create -o encryption=on -o keyformat=passphrase mypool/myencrypteddata
```

```bash
# raw key instead of passphrase
sudo dd if=/dev/random of=/root/mykey bs=32 count=1
sudo zfs create -o encryption=on -o keyformat=raw -o keylocation=file:///root/mykey mypool/myencrypteddata
```

## Load
```bash
sudo zfs load-key mypool/myencrypteddata
```

## Unload
```bash
sudo zfs unload-key mypool/myencrypteddata
```

## Change Key
```bash
sudo zfs change-key mypool/myencrypteddata
```