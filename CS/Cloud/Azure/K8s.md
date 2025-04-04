---
tags:
  - cloud
  - k8s
  - infra
title: K8s
---
- [Azure AD Workload Identity](https://azure.github.io/azure-workload-identity/docs/)
- EKS Service Accounts -> Roles
- Managed Identities
	- "Managed identities for Azure resources are the recommended way to authorise access from an AKS cluster to other Azure services"
	1. System Assigned
		- Single Azure resource (AKS cluster)
		- Exists for lifecycle of cluster only
		- Repo access (presumably)
	2. User Assigned
		- Standalone resource you manage
		- Managed separately to cluster
		- Can be used by multiple resources
	3. Pre-Created Kubelet
		- Optional
		- User assigned identity
		- If no user assigned identity is assigned for the kubelet, one is created
	- "By assigning an Azure RBAC role to the managed identity, you can grant your cluster permissions to access specific resources. For example, you can assign the managed identity an Azure RBAC role that allows it to access secrets in an Azure Key Vault. This way, you can easily authorize access to your cluster without managing credentials."

| Identity                                              | Use Case                                                                                            | Default Permissions                                                                                                                         |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Control Plane<br>(system-assigned)                    | Manage cluster resources<br>Ingress Load Balancers, AKS public IPs, Cluster autoscaler, CSI drivers | Contributor role for node resource group                                                                                                    |
| Kubelet                                               | Azure Container Repo                                                                                | N/A                                                                                                                                         |
| Add-on Identities<br>- NPM<br>- CNI<br>- Azure Policy | None                                                                                                | N/A                                                                                                                                         |
| Application Routing                                   | Azure DNS & Azure Key Vault Certs                                                                   | Key Vault Secrets User role for Key Vault, DNS Zone Contributor role for DNS zones, Private DNS Zone Contributor role for private DNS zones |
| Ingress Application Gateway                           | Manages required network resources.                                                                 | Contributor role for node resource group                                                                                                    |
| Workload identity (Microsoft Entra Workload ID)       | Enables applications to securely access cloud resources with Microsoft Entra Workload ID.           | N/A                                                                                                                                         |
# Microsoft Entra Workload ID for Kubernetes
- Service Account -> Entra Workload ID
- Uses OIDC like AWS