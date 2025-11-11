# Azure Virtual Machine (VM)

## Overview
An **Azure Virtual Machine (VM)** is an **on-demand, scalable computing resource** provided by Microsoft Azure.

## Key Points
- Provides **virtualized hardware** such as **CPU, memory, storage, and networking**.
- Used to **run operating systems and applications** like a physical computer.
- Part of **Infrastructure as a Service (IaaS)** in Azure.
- Supports both **Windows** and **Linux** operating systems.
- You can **start, stop, scale, or delete** VMs anytime.
- Commonly used for:
  - **Hosting websites**
  - **Development and testing**
  - **Backup and disaster recovery**

## Example Use Cases
- Deploying web servers
- Running custom applications
- Creating isolated development environments

# Difference Between Azure Region and Availability Zone
## Key Differences

| Feature | Region | Availability Zone |
|----------|--------|-------------------|
| **Definition** | Geographical area with multiple data centers | Individual data center within a region |
| **Purpose** | To group Azure resources geographically | To ensure high availability within a region |
| **Fault Isolation** | Between different regions | Between zones in the same region |
| **Example** | Central India, East US | Zone 1, Zone 2, Zone 3 (inside Central India region) |


# Azure Virtual Network (VNet) –

## 1. What is a Virtual Network?  
Azure Virtual Network (VNet) is the fundamental building block for your private network in Azure. It enables Azure resources (such as VMs) to securely communicate with each other, the internet, and on-premises networks. :contentReference[oaicite:0]{index=0}  
It delivers scale, availability, and isolation benefits while using familiar networking concepts from traditional datacentres. :contentReference[oaicite:1]{index=1}

---

## 2. Why Use a Virtual Network?  
Key scenarios you can achieve with a VNet: :contentReference[oaicite:2]{index=2}  
- Communication of Azure resources with the internet.  
- Communication between Azure resources.  
- Communication with on-premises resources.  
- Filtering of network traffic.  
- Routing of network traffic.  
- Integration with Azure services.

---

## 3. Communication Scenarios  
### a) With the Internet  
- All resources in a VNet can by default communicate outbound with the internet. :contentReference[oaicite:3]{index=3}  
- For inbound access, assign a public IP address or a public load balancer. :contentReference[oaicite:4]{index=4}  
- If only an internal standard load balancer is used, outbound connectivity isn’t available until you define how outbound will work. :contentReference[oaicite:5]{index=5}

### b) Between Azure Resources  
- You can deploy VMs and other Azure resources (e.g., AKS, VM scale sets) into a VNet. :contentReference[oaicite:6]{index=6}  
- **Service endpoints**: Extend the VNet’s private address space to Azure service resources, securing the service to only your VNet. :contentReference[oaicite:7]{index=7}  
- **VNet peering**: Connect two VNets (same or different regions/subscriptions) so resources communicate as if in the same network. :contentReference[oaicite:8]{index=8}

### c) With On-Premises Resources  
- **Point-to-Site VPN**: Connects a single computer to the VNet. Useful for dev/test or individual devices. Secure tunnel over the internet. :contentReference[oaicite:9]{index=9}  
- **Site-to-Site VPN**: Between on-premises VPN device and Azure VPN gateway. Encrypted tunnel over the internet. :contentReference[oaicite:10]{index=10}  
- **Azure ExpressRoute**: Private dedicated connection between your network and Azure. Traffic doesn’t go over the internet. :contentReference[oaicite:11]{index=11}

---

## 4. Traffic Control & Routing  
### a) Filter Network Traffic  
- **Network Security Groups (NSG)** & **Application Security Groups (ASG)**: Define inbound/outbound security rules by source/destination IP, port, protocol. :contentReference[oaicite:12]{index=12}  
- **Network Virtual Appliances (NVA)**: Deploy virtual machines that perform network functions (e.g., firewall, WAN optimization) in the VNet. :contentReference[oaicite:13]{index=13}

### b) Route Network Traffic  
- Azure provides default routing between subnets, VNets, on-premises, and internet. :contentReference[oaicite:14]{index=14}  
- You can override default routes via:  
  - **Custom route tables** per subnet. :contentReference[oaicite:15]{index=15}  
  - **BGP route propagation** if using VPN gateway or ExpressRoute. :contentReference[oaicite:16]{index=16}

---

## 5. Integration with Azure Services  
- You can deploy **dedicated instances** of Azure services into your VNet so they are privately accessible. :contentReference[oaicite:17]{index=17}  
- **Azure Private Link**: Access specific service instances privately from your VNet (and from on-premises). :contentReference[oaicite:18]{index=18}  
- **Service Endpoints**: Extend your VNet to Azure services via their public endpoints, and secure those services to your VNet. :contentReference[oaicite:19]{index=19}

---

## 6. Limits, Zones & Pricing  
- VNets and subnets span all availability zones in a region; you don’t need separate VNets by zone. :contentReference[oaicite:20]{index=20}  
- There are limits on networking resources (number of VNets, subnets, peers etc). Many limits are max values and you can request increases. :contentReference[oaicite:21]{index=21}  
- VNet itself is free-of-charge. Charges apply for resources you deploy in/with the VNet (VMs, gateways, etc.). :contentReference[oaicite:22]{index=22}

---

## 7. Key Terminology Cheat Sheet  
- **VNet** – Virtual Network in Azure  
- **Subnet** – Division within a VNet for resource grouping  
- **NSG** – Network Security Group  
- **ASG** – Application Security Group  
- **VNet Peering** – Linking VNets together  
- **VPN Gateway** – For site-to-site or point-to-site connections  
- **ExpressRoute** – Private dedicated link to Azure  
- **Custom Route Table** – For overriding default routing  
- **Private Link / Service Endpoint** – Private access to Azure services  

---


