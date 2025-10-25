---
title: RBAC
tags:
  - k8s
---
# `Role`
- Namespaced
- Defines permissions to k8s resources by namespace
# `ClusterRole`
- Not-namespaced
- Defines permissions cluster-wide

# Role Bindings
- Roles & Cluster Roles -> Users/Groups/Service Accounts
- `RoleBinding`
- `ClusterRoleBinding`
- Using `roleRef` field