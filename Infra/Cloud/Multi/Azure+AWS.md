---
date: 2026-03-06
title: Azure & AWS
tags:
  - cloud/aws
  - cloud/azure
---
# Peering
[AWS Blogs - Designing private network connectivity between AWS and Microsoft Azure](https://aws.amazon.com/blogs/modernizing-with-aws/designing-private-network-connectivity-aws-azure/)
- [AWS Site-to-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html) over the public internet.
- [AWS Direct Connect](https://aws.amazon.com/directconnect/) and Azure ExpressRoute in customer-managed infrastructure.
- AWS Direct Connect and Azure ExpressRoute in a facility with a multicloud connectivity provider.

![](https://d2908q01vomqb2.cloudfront.net/8effee409c625e1a2d8f5033631840e6ce1dcb64/2024/01/16/multi-vpc-vpn-azure-aws.jpg)

- In AWS:
    - Virtual private gateway, which is the router on the AWS side of the VPN tunnel.
    - Customer gateway, which is the public IP of the Azure virtual network gateway.
- In Azure:
    - Azure VPN gateway, which is used to send encrypted traffic to/from an Azure vNet over the public internet.
    - Local network gateway, which routes to a VPN endpoint in AWS. Two are required for redundancy.