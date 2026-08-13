---
title: LVM
date: 2026-08-12
---
```bash
sudo lvresize -l +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
sudo resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv
```
