# Azure Virtual Machine (VM)

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
<img width="844" height="276" alt="image (3)" src="https://github.com/user-attachments/assets/33b633a4-94e2-4d61-a015-46acbdf91412" />

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

# What is Azure Bastion?
Azure Bastion is a fully managed PaaS service that you provision to securely connect to virtual machines via private IP address. It provides secure and seamless RDP/SSH connectivity to your virtual machines directly over TLS from the Azure portal, or via the native SSH or RDP client already installed on your local computer. When you connect via Azure Bastion, your virtual machines don't need a public IP address, agent, or special client software.
Bastion provides secure RDP and SSH connectivity to all of the VMs in the virtual network for which it's provisioned. Using Azure Bastion protects your virtual machines from exposing RDP/SSH ports to the outside world, while still providing secure access using RDP/SSH.

<img width="1861" height="700" alt="image" src="https://github.com/user-attachments/assets/633971d8-804f-4716-8ed3-e6299d73f7b7" />
