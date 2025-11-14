# Vnet Peering Different AZ

## STEP 1 — Create VNet 1 (Region 1)
1. click on vertual Network
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2cc987c7-e66b-4248-b097-698dbcd1b1b8" />
2. click on create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b5540a1c-667d-40a2-8b2b-4dcd1c7fa12a" />
3. Select Resource Group: `pratham`
4. Type VNet Name: `VNET10`
5. Select Region: `Central India`
6.  Go to **IP Addresses** tab
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/be42924d-32b9-434e-8038-fef3724f2af7" />
7. Click **Add Subnet**
8. IP Address Range: `10.0.0.0/16`
9. Subnet Range: `10.0.1.0/24`
10. Click **Add**
11. Click **Review + Create**
![image](https://github.com/user-attachments/assets/58f82d68-e732-48fd-baaa-9cd2be9bc676)

# 📌 **Step 2 — Create Second VNet2 (20 Network)**

1. Click **Virtual Network**
2. Click **Create**
<img width="1919" height="1001" alt="image" src="https://github.com/user-attachments/assets/933564a6-82b9-427c-b157-f8d046438939" />
3. Select Resource Group: `pratham`
4. VNet Name: `VNET20`
5. Region: `EAST ASIA`
6. Go to **IP Addresses** tab
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/00af027e-9ccb-454f-a220-588ecd4b01bb" />
7. Click **Add Subnet**
8. IP Range: `20.0.0.0/16`
9. Subnet Range: `20.0.1.0/24`
10. Click **Add**
11. Click **Review + Create**
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/65825cd1-0387-4589-a39b-0ddc7b555249" />

# 📌 **Step 3 — Create Windows VM1 in VNet10**

1. Click **Virtual Machines**
   ![image](https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045)

2. Click **Create → Virtual Machine**
   ![image](https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b)
3. Resource Group: `pratham`
4. VM Name: `VNET10` 
5. Region: `Central India`
6. Availability Zone: `3`
<img width="1919" height="1065" alt="image" src="https://github.com/user-attachments/assets/5af6ce9f-20cc-42cc-bdbc-322255e0e36c" />
7. Image: Windows Server
8. Select Size
 <img width="1919" height="1072" alt="image" src="https://github.com/user-attachments/assets/a6549bcc-752c-484e-a133-59914e07a64a" />
9. Username: `VNET10`
10. Password: ******
11. Inbound Port Rule → Select **RDP (3389)**
12. Click Next: Disk
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/dacd2d7c-117a-4615-a94f-779857a53f23" />
13. Go to **Networking**
![image](https://github.com/user-attachments/assets/ca5fb417-e254-4641-8439-4410a0d36c9b)
14. Select VNet: `VNET10`
15. Click **Review + Create**
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0a66fadb-bac9-44b3-a6bb-0e5ed6c1570b" />
16. Click **Create**
<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/24bf946e-907b-4c6b-9d0e-caf03c5cf403" />


# 📌 **Step 3 — Create Windows VM2 in VNET20**

1. Click **Virtual Machines**
   ![image](https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045)

2. Click **Create → Virtual Machine**
   ![image](https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b)
3. Resource Group: `pratham`
4. VM Name: `VNET20` 
5. Region: `EAST AISA`
6. Availability Zone: `1`
<img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/d44ee747-44d6-4f36-b811-98d5df576d19" />
7. Image: Windows Server
8. Select Size
 <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/073cc8dc-cef2-40eb-85fc-af1c995777aa" />

9. Username: `VNET20`
10. Password: ******
11. Inbound Port Rule → Select **RDP (3389)**
12. Click Next: Disk
<img width="1919" height="1063" alt="image" src="https://github.com/user-attachments/assets/dd389fde-5043-438a-8ee9-d95712a9bcc9" />
13. Go to **Networking**
![image](https://github.com/user-attachments/assets/ca5fb417-e254-4641-8439-4410a0d36c9b)
14. Select VNet: `VNET20`
15. Click **Review + Create**
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b9f0bd77-7f73-49e3-b9c9-e9511cc5db4f" />

16. Click **Create**
<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/24bf946e-907b-4c6b-9d0e-caf03c5cf403" />

# 📌 **Step 4 — Create VNet Peering**
1. Click **Virtual Networks**
   ![image](https://github.com/user-attachments/assets/5070d5db-15ac-4b9d-9fdf-136c17482378)
2. Select **VNET10**
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/4b6d0587-b4ef-4099-86f7-baa061b4ab08" />
3. Go to **Settings → Peerings**
   <img width="1917" height="1079" alt="image" src="https://github.com/user-attachments/assets/27429735-f046-453d-85fb-1ec7ab7a2447" />
4. Click **Add**
   ![image](https://github.com/user-attachments/assets/8b4c2735-dc3a-41f2-aafa-964b41afa874)
5. Peering Name: `VNET10-TO-VNET20`
6. Remote VNet: `VNET20`
   <img width="1917" height="1053" alt="image" src="https://github.com/user-attachments/assets/ffe4bfc5-04b6-4ea6-b3fd-c874d56e593e" />
7. Local Peering Name: `VNET20-TO-VNET10`
8. Click **Add**
   <img width="1919" height="1067" alt="image" src="https://github.com/user-attachments/assets/4731982b-8ddf-4ff3-86a3-87ffeacbf447" />


# 📌 **Step 5 — Connect Both VMs using RDP**

1. Click **Virtual Machines**
2. Open VNET10 VM
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/74d3415a-1a51-46de-a417-0c0b0419a394" />
3. Click **Connect**
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/4be3b313-670f-4ae6-8075-1711b20b871c" />
4. Copy Public IP
5. Open **Remote Desktop Connection**
   ![image](https://github.com/user-attachments/assets/acdb9bc0-eae4-4c7a-aa7d-d617a08aae5c)
6. Paste Public IP → Connect
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/bb5fb724-3d6b-4cee-9d20-ace27742d6ae" />
7. Enter Username + Password
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/742d5ba5-f364-4abd-8cbb-8cc990b79fdb" />
8. Click Yes

   ![image](https://github.com/user-attachments/assets/082bd01f-65ea-4ff1-b9a7-635f9d4af62b)

## Same steps for VM20.

# 📌 **Step 6 — Enable ICMP comunication port for private ip in Both VMs**
1. click on window icone
2. go to server manager
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f683bc0e-e2c8-4504-a0a1-ac9dfe43ad21" />
3. click on tools
4. click on window difendar firewall with adwance security
<img width="1919" height="1067" alt="image" src="https://github.com/user-attachments/assets/342127fc-2f7f-48b0-9d72-f008e7da6a02" />
5. click on inbound rule
6. click on new rule
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1f497e07-4a84-4699-b9c2-edfc9737b9b9" />

7. chose custom
8. click next
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/c425833b-e696-4346-80fb-f9ab6fd3bbb4" />
9. go to protocall and port
10. chose ICMPv4
11. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b6c431a1-e58e-4bbf-89a0-b4e2daa1c918" />
12. click until next to name
13. type name `ICMP` 
14. click finish
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0de194d8-e709-4f70-9c6a-06e6a9970da7" />


# 📌 **Step 6 — Enable ICMP comunication port for public ip in Both VMs**

1. Click **Virtual Machines**
2. Open VNET10 VM
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/74d3415a-1a51-46de-a417-0c0b0419a394" />
3. CLICK ON NETWORK
4. GO TO NETWORK SETTING
5. CLICK ON CREATE PORT RULE
6. CLICK ON INBOUND PORT RULE
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/58bab089-82b9-4be2-bc1e-f6f3533503e7" />
7. SELECT PROTOCAL: `ICMPV4`
8. ACTION: `ALLOW`
9. CLICK ON ADD
<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/995de4fd-3e6e-4481-a30e-de7b724693e3" />

## Same steps for VM20.

# 📌 **Step 7 Ping Test
## ping on private ip

### **On VM20:**

1. Open command prompt

2. Run:

   ```
   ping 10.0.2.4
   ```
   <img width="1920" height="1069" alt="image" src="https://github.com/user-attachments/assets/ccb7d694-be57-421b-aef2-2fe6ecd5c9d6" />

## ping on public ip

1. Open command prompt

2. Run:

   ```
   ping 10.0.2.4
   ```

   <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d48f6860-9238-47ba-a889-eb43f463b7a8" />
