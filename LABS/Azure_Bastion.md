# Azure Bastion Setup (Full Step-by-Step with Images)

# 🟦 **Step 1 — Create Virtual Network for Bastion**

1. Click **Virtual Network**
   ![](https://github.com/user-attachments/assets/9acbf209-4afd-4170-910a-63c82d3256e0)

2. Click **Create**
   ![](https://github.com/user-attachments/assets/bdfa34e6-7c5c-497b-89ea-69a505b49973)

3. Resource Group: `Pratham`

4. VNet Name: **Bastion-vnet**

5. Region: **Central India**

6. Click **IP Addresses**
   ![](https://github.com/user-attachments/assets/094036cf-6d5e-4d12-b23d-5f2161ae431e)

7. Click **Add Subnet**

8. Subnet Purpose: **Azure Bastion**

9. Address Range: `40.0.1.0/24`

10. Click **Save**

11. Click **Review + Create**
    ![](https://github.com/user-attachments/assets/5d27c551-a8d8-4884-80db-03f0b98cf2da)

12. Click **Create**
    ![](https://github.com/user-attachments/assets/ed1f32b6-355f-4d16-b4d1-d761665b74ac)

---

# 🟩 **Step 2 — Create Windows VM (Without Public IP)**

1. Click **Virtual Machines**
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)

2. Click **Create → Virtual Machine**
   ![](https://github.com/user-attachments/assets/37cc27f8-d7af-4813-bc19-04d06f5373b9)

3. Resource Group: `Pratham`

4. VM Name: **Bastion-VM**

5. Region: **Central India**

   ![](https://github.com/user-attachments/assets/15b506ed-e143-4ba8-96dc-538a9ce11c32)

6. Choose Image: **Windows Server**

7. Choose Size
   ![](https://github.com/user-attachments/assets/9015c3c3-e011-4e21-98a8-3c8e84f189b9)

8. Username: `Bastion-VM`

9. Password: `********`

10. Inbound Port: **RDP (3389)**

11. Click **Next: Disk**
    ![](https://github.com/user-attachments/assets/1fd9a948-e8fd-4d11-8e52-5fb3885e6aee)

12. Click **Networking**
    ![](https://github.com/user-attachments/assets/a11a6227-d7bd-4c45-b0f2-ac6a0e038fed)

13. Virtual Network: **Bastion-Vnet**

14. Subnet: **Default**

15. Public IP: **None**

16. Click **Review + Create**
    ![](https://github.com/user-attachments/assets/7deccdb2-1d1b-4cd8-902b-281fc4aa9c09)

17. Click **Create**
    ![](https://github.com/user-attachments/assets/1f5450fd-d656-409d-81fd-248357486f31)

---

# 🟥 **Step 3 — Create Azure Bastion Host**

1. Search **Bastion** in Azure Search Bar.

2. Click **Bastions**
   ![](https://github.com/user-attachments/assets/127d990c-5c5a-4e3a-a04e-28008eb1d5cc)

3. Click **Create**
   ![](https://github.com/user-attachments/assets/8dde39ad-a561-4522-a581-e71acc857a9c)

4. Resource Group: `Pratham`

5. Bastion Name: **Bastion**

6. Region: **Central India**

   ![](https://github.com/user-attachments/assets/d38caffc-97a9-478e-ae7d-e195e4efa523)

7. Virtual Network: **Bastion-Vnet**

8. Public IP: Select **Create New**

9. Click **Review + Create**
   ![](https://github.com/user-attachments/assets/3e2a5763-84d1-4d1c-a959-654b27f51394)

10. Click **Create**
    ![](https://github.com/user-attachments/assets/4b9ba38a-fd4e-45d8-b836-12350cc26f01)

---

# 🟦 **Step 4 — Connect to VM Using Azure Bastion**

1. Click **Virtual Machines**
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)

2. Open VM: **Bastion-VM**
   ![](https://github.com/user-attachments/assets/b72fc8e0-7e34-425b-b9e6-24a13689e0a8)

3. Click **Connect** → **Connect via Bastion**
   ![](https://github.com/user-attachments/assets/18015234-7438-4ed9-92e3-54d7017831ae)

4. Username: `Bastion-VM`

5. Password: `********`

6. Click **Connect**
   ![](https://github.com/user-attachments/assets/7597edbb-a892-4d69-8016-a198183ff111)

7. VM successfully connected through Bastion
   ![](https://github.com/user-attachments/assets/ab509358-125a-4397-8a3b-6825f55f3ec3)

---

# 🎉 **Azure Bastion Setup Completed Successfully!**

