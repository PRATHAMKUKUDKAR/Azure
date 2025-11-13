# Azure Virtual Machine (VM)
## Overview
An **Azure Virtual Machine (VM)** is an on-demand computer that runs on Azure’s cloud.  
It works like a physical computer and allows you to run Windows/Linux OS and applications.

## Key Points
- Part of **Infrastructure as a Service (IaaS)**
- Provides CPU, RAM, storage, and networking
- You can start, stop, scale, or delete anytime
- Supports **Windows & Linux**
- Used for:
  - Hosting websites/applications
  - Development & testing
  - Backup and disaster recovery

---

# Azure Region vs Availability Zone

| Feature | Region | Availability Zone |
|--------|--------|--------------------|
| Definition | Geographic area with multiple data centers | Individual data centers within a region |
| Purpose | To deploy Azure resources geographically | High availability inside a region |
| Fault Isolation | Between regions | Between zones in the same region |
| Example | Central India, East US | Zone 1, Zone 2, Zone 3 |

---

# Azure Virtual Network (VNet)

## What is a VNet?
A **VNet** is a private network in Azure used to connect virtual machines and other Azure resources securely.

## Why use a VNet?
- Secure communication between Azure resources  
- Connect Azure to the internet  
- Connect Azure to on-premises (via VPN or ExpressRoute)  
- Control traffic using NSG (firewall rules)

## Communication Types
- **VM ↔ Internet:** Needs Public IP for inbound  
- **VM ↔ VM:** Same VNet or via VNet Peering  
- **Azure ↔ On-Premises:** Using P2S VPN, S2S VPN, or ExpressRoute

---

# Azure VNet Peering

## What is VNet Peering?
VNet Peering connects two VNets so that their resources communicate **privately and directly** over Azure’s backbone network.

## Why use it?
- Very fast (low latency)
- Secure (no public internet)
- No VPN gateway required (cost saving)
- Works across same region or different regions

## Types of Peering
1. **Regional Peering** – Same region  
2. **Global Peering** – Different regions  

## Benefits
- Private, secure connection  
- High performance  
- No downtime  
- Multi-tier and multi-region apps can communicate  

