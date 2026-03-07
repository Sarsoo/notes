---
title: Active Directory
tags:
  - infra/windows
---
#net
[MSDocs Overview](https://docs.microsoft.com/en-us/windows/security/identity-protection/access-control/access-control)

# Security Principal
- Entity that can be authenticated
- Users & groups
- Have security identifier
	- SID
- Assigned rights & permissions

# Resources
- Have owner
	- Grants permissions to other security principals
- Types
	- Files
	- Folders
	- Printers
	- Registry keys
	- AD domain services objectsr
- Access control lists

```powershell
gpresult /r /SCOPE COMPUTER
```
```powershell
gpupdate /force
```
