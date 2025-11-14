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

# 📌 **Step 2 — Create Second VNet (20 Network)**

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

# 📌 **Step 3 — Create Windows VM in VNet10**

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


# 📌 **Step 3 — Create Windows VM in VNET20**

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

