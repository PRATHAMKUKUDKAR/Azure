# 🔥 Azure Firewall + Windows VM + Application Rule Full Setup Guide  

This documentation explains how to deploy:

- ✔ 1 Virtual Network  
- ✔ Subnet for Virtual Machine  
- ✔ Subnet for Azure Firewall  
- ✔ Windows Server VM  
- ✔ Azure Firewall (Standard)  
- ✔ Application Rule to allow specific FQDN (google.com)  
- ✔ Route Table to force traffic through Firewall  

All steps include screenshots for better understanding.

---
# Diagram
<img width="1338" height="843" alt="image" src="https://github.com/user-attachments/assets/7a93c9dc-1e40-4658-8153-13804a4e0444" />

---

# 🚀 STEP 1 — Create Virtual Network (VNet)

### 1. Open **Virtual Network**
![](https://github.com/user-attachments/assets/2cc987c7-e66b-4248-b097-698dbcd1b1b8)

### 2. Click **Create**
![](https://github.com/user-attachments/assets/b5540a1c-667d-40a2-8b2b-4dcd1c7fa12a)

### 3. Fill Basic Details
- **Resource Group:** `pratham`
- **VNet Name:** `VNET`
- **Region:** `Central India`

### 4. Go to **IP Addresses** tab
![](https://github.com/user-attachments/assets/591b61d7-7d1f-4aeb-bfcf-0a7c0d1d2be4)

---

## ➤ Create Subnet1 (For VM)

### 5. Click **Add Subnet**
### 6. Click edit ✏️ icon  
### 7. Enter details:
- **Subnet Name:** `SUBNET1`
- **VNet Range:** `10.0.0.0/16`
- **Subnet Range:** `10.0.1.0/24`

![](https://github.com/user-attachments/assets/7cfd3e86-82af-4850-92e5-97cf242380ea)

---

## ➤ Create Azure Firewall Subnet

### 8. Click **Add Subnet**
- **Subnet Purpose:** `Azure Firewall`
- **Name:** `AzureFirewallSubnet`
- **VNet Range:** `10.0.0.0/16`
- **Subnet Range:** `10.0.2.0/24`

![](https://github.com/user-attachments/assets/c4e0d770-b1ae-4918-9549-71c689511059)

### 9. Click **Review + Create**
### 10. Click **Create**

![](https://github.com/user-attachments/assets/7d424c66-3279-4bf3-b98b-2020625e1ffa)

---

# 💻 STEP 2 — Create Windows Server VM

### 1. Click **Virtual Machines**
![](https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045)

### 2. Click **Create → Virtual Machine**
![](https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b)

### 3. Fill Basic Details
- **Resource Group:** `pratham`
- **VM Name:** `VM`
- **Region:** `Central India`
- **Availability Zone:** 3

![](https://github.com/user-attachments/assets/ff25d1ae-4543-48f2-a766-91e25a16c7e0)

### 4. Select Image & Size
![](https://github.com/user-attachments/assets/eeaa1131-8132-493a-b8bd-58d6679396bc)

### 5. Provide Credentials
- Username: `VM`
- Password: `*******`

### 6. Enable **RDP (3389)**
### 7. Click **Next: Disk**
![](https://github.com/user-attachments/assets/8e37feff-a0da-4904-9b8a-8ebd80ddf378)

### 8. Networking
- Select VNet → `VNET`
- Select Subnet → `SUBNET1`

![](https://github.com/user-attachments/assets/540bc0c0-0852-4eb3-a184-6b4375c2297a)

### 9. Click **Review + Create** → **Create**
![](https://github.com/user-attachments/assets/b15c5f29-c5ef-45f7-b0ec-f01ef85e128f)

---

# 🔥 STEP 3 — Create Azure Firewall

### 1. Search **Firewall**
![](https://github.com/user-attachments/assets/7e837283-14bc-4d87-bb21-c580b0f1d318)

### 2. Click **Create**
![](https://github.com/user-attachments/assets/1f6ce662-20a5-4fb6-a80a-dcb6f1051f7f)

### 3. Fill Details
- **Resource Group:** `pratham`
- **Name:** `FIREWALL`
- **Region:** `Central India`
- **SKU:** `Standard`

![](https://github.com/user-attachments/assets/fb03804a-987a-4c0c-8e52-bbe8f19cb1bb)

### 4. Configuration
- Firewall management → **Use firewall rules (classic)**
- Virtual network → **Use existing**
- Select VNet → `VNET`
- Create Public IP → `FIREWALL-IP-PUB`

![](https://github.com/user-attachments/assets/eb37ca82-2167-436b-8049-ca8561aeae3e)

### 5. Disable Firewall Management NIC
![](https://github.com/user-attachments/assets/fae1e142-148f-4bc5-9ff1-7f02c7c458f9)

### 6. Click Review + Create → Create
![](https://github.com/user-attachments/assets/989a68ff-2e9c-4e98-b323-c5b2381860a9)

---

# 🔥 STEP 4 — Add Application Rule

### 1. Go to Firewall → **Rules (Classic)**  
### 2. Click **Add Application Rule Collection**
![](https://github.com/user-attachments/assets/27618efd-e553-4cb2-935c-1a2063e7d128)

### 3. Enter Rule Details  
- Name: `Application`
- Priority: `200`
- Action: `Allow`
- Rule Name: `App-Allow`
- Source Type: `IP Address`
- Source: `*` (any IP)
- Protocol: `http:80, https:443`
- Target FQDNs: `google.com`

---

# 🔥 STEP 5 — Create Route Table

### 1. Go to **Route Tables**
### 2. Click **Create**

![](https://github.com/user-attachments/assets/cfa1fd7f-b6c9-49e8-9de8-4eeaf1f5de20)

### 3. Fill Details
- Resource Group: `Pratham`
- Region: `Central India`
- Name: `RT`

### 4. Click **Review + Create**
![](https://github.com/user-attachments/assets/823950a8-653a-4352-92b8-2325a0e00be9)

### 5. Click **Create**
![](https://github.com/user-attachments/assets/4d46bb28-b845-4f92-9aac-c0d426abf0b8)

---

## ➤ Add Route

### 6. Go to Route Table → Routes → Add
- Route Name: `Firewall-to-Internet`
- Destination Type: `IP Address`
- Destination: `0.0.0.0/0`
- Next Hop Type: `Virtual Appliance`
- Next Hop Address: `10.0.2.0` (Firewall Private IP)

![](https://github.com/user-attachments/assets/f211bbfa-8e71-4a89-9ba2-c5608ed18ff0)

---

## ➤ Associate Subnet

### 7. Go to **Subnets → Associate**
![](https://github.com/user-attachments/assets/795a0c6f-7212-43f9-88b7-daa556252efc)

- Virtual Network: `VNET`
- Subnet: `AzureFirewallSubnet`

![](https://github.com/user-attachments/assets/1ab5a516-6e4d-45a6-bc6b-923475665456)

---

# 🟢 STEP 6 — Connect via RDP

### 1. Open Remote Desktop  
![](https://github.com/user-attachments/assets/e57bc33b-a42b-4321-95e9-2f625e00e74a)

### 2. Enter **Firewall Public IP**
![](https://github.com/user-attachments/assets/704fee5d-16ed-4413-b807-211a1d3eac63)

### 3. Enter VM Credentials  
![](https://github.com/user-attachments/assets/07b1262d-3cd2-4b1c-8e0f-52daacdacf59)

### 4. SUCCESS — VM Connected Successfully!  
![](https://github.com/user-attachments/assets/a8541fbb-cfc5-404f-a17b-ad12530f02d9)

---

# 🟧 STEP 7 — Verify Application Rule

### 1. Open Microsoft Edge on VM  
### 2. Search `www.google.com` → It works  
![](https://github.com/user-attachments/assets/2c2e354b-3e77-46f3-85f1-507dcf01a1e1)

### 3. Search any other website → It does NOT work  
![](https://github.com/user-attachments/assets/669f4dc0-307f-4e30-9068-ffe5a15d78c8)

---

# 👑 Author  
**Pratham**
