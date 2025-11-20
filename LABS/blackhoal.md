# 🔐 Azure NSG Internet Block Lab 
This lab demonstrates how to:

- ✔ Create a Virtual Network  
- ✔ Create a Windows Server VM (No Public IP)  
- ✔ Create an NSG rule to block all outbound internet traffic  
- ✔ Access VM securely using Azure Bastion  
- ✔ Verify that the internet is blocked  

All steps include screenshots for better understanding.

---

# 🟦 Step 1 — Create Virtual Network for Bastion

1. Click **Virtual Network**  
   ![](https://github.com/user-attachments/assets/9acbf209-4afd-4170-910a-63c82d3256e0)

2. Click **Create**  
   ![](https://github.com/user-attachments/assets/bdfa34e6-7c5c-497b-89ea-69a505b49973)

3. Resource Group: `Pratham`

4. VNet Name: **Vnet**

5. Region: **Central India**

6. Click **IP Addresses** tab  
   ![](https://github.com/user-attachments/assets/8926d4b1-be86-4243-bfd5-feb4089227f7)

7. Keep the default subnet as it is.

8. Click **Add Subnet**

9. Subnet Purpose: **Azure Bastion**

10. Address Range: `10.0.1.0/24`

11. Click **Save**

12. Click **Review + Create**  
   ![](https://github.com/user-attachments/assets/75498202-422a-45bb-82e4-088d084c0f5d)

13. Click **Create**  
   ![](https://github.com/user-attachments/assets/a54eef3f-8c96-4008-84db-865c3628d348)

---

# 🟩 Step 2 — Create Windows VM (Without Public IP)

1. Click **Virtual Machines**  
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)

2. Click **Create → Virtual Machine**  
   ![](https://github.com/user-attachments/assets/37cc27f8-d7af-4813-bc19-04d06f5373b9)

3. Resource Group: `Pratham`

4. VM Name: **VM**

5. Region: **Central India**  
   ![](https://github.com/user-attachments/assets/474d0884-1fc0-404d-8953-67bd300df8c8)

6. Image: **Windows Server**

7. Choose VM Size  
   ![](https://github.com/user-attachments/assets/ac75eb19-3c9f-4980-a41d-a74c97bb389f)

8. Username: `VM`  
9. Password: `********`

10. Enable inbound port: **RDP (3389)**

11. Click **Next: Disk**  
   ![](https://github.com/user-attachments/assets/2a83f5a9-4e1c-4dde-92f9-c38b1e11a0b7)

12. Go to **Networking**

13. Select VNet → **Vnet**

14. Select Subnet → **Default**

15. Public IP: **None**

16. Click **Review + Create**  
    ![](https://github.com/user-attachments/assets/c66d4e85-a237-4729-bd38-5ae2f278752c)

17. Click **Create**  
    ![](https://github.com/user-attachments/assets/55b62440-f4f5-41bd-bbac-37c9f62f1bf4)

---

# 🟥 Step 3 — Create Blackhole Route Using Route Table (Internet BLOCK RULE)

1. click on Search Bar
2. type route
3. click on Route Table
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/87b52293-26ad-493b-8a87-3051f498bb9e" />
4. click on Create
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4175eaa6-3001-4f60-a41c-eda54028d21a" />
5. type Resource Group: `Pratham`
6. Select Region: `Central India`
7. type name: `Internet-Blackhole-RT`
8. click on Rewie + Create
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f81b3676-147e-4a06-ad07-720b5596535d" />
9. click on Create
    <img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/a1ee7f87-cc94-4717-a20c-74bda5cfa5fb" />

10. click on Go to resources
    <img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/224853c7-9a69-4891-8990-60e2b43e3c88" />

11. click on Internet-Blackhole-RT
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3371566c-f7c4-4d20-93bb-7faf29f1938b" />
12 click on routes
13. click on Add
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2134094e-2813-4899-9ae8-704ac122314f" />

14. type route name: `deny-internet`
15. choose Destination type: `ip Adrress`
16. type destination ip Adrress type/CIDR Range: `0.0.0.0/0`
17. Next Hope Type: `None`
18. click on Add
    <img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/81117130-ff95-4b2c-a390-21c78e39ee98" />

# 🟥 Step 4 — Associate Route Table to VM Subnet

1. click on Subnet
2. click on Associate
3. Select Vertual Network: `Vnet`
4. Select Subnet: `defalte`
5. click on Ok
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6ad86c88-974d-4446-ab30-44e1e486b5f2" />




# 🟦 Step 4 — Connect to VM Using Bastion

1. Click **Virtual Machines**  
2. Select VM  
3. Click **Connect → Bastion**  
   ![](https://github.com/user-attachments/assets/a006d4f5-d217-4501-b902-19b7b16f4a50)

4. Enter:
- Username: `vm`  
- Password: `********`

5. Click **Connect**

6. VM Login Successful  
   ![](https://github.com/user-attachments/assets/f8a71bf1-d7eb-4f68-9ee1-1e7ed2935b77)

---

# 🟩 Step 5 — Verify Internet Is Blocked

1. Open **Microsoft Edge**  
   ![](https://github.com/user-attachments/assets/190c063a-ffdb-4fe4-a957-07ae82a51763)

2. Search any website → **It will NOT open**  
  <img width="1919" height="947" alt="image" src="https://github.com/user-attachments/assets/8456502b-a69d-43ed-b4f7-74f59ad83eef" />


---

# 👑 Author  
**Pratham**
