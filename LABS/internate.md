# 🟦 Step 1 — Create Virtual Network for Bastion

1. Click **Virtual Network**  
   ![](https://github.com/user-attachments/assets/9acbf209-4afd-4170-910a-63c82d3256e0)

2. Click **Create**  
   ![](https://github.com/user-attachments/assets/bdfa34e6-7c5c-497b-89ea-69a505b49973)

3. Resource Group: `Pratham`

4. VNet Name: **Vnet**

5. Region: **Central India**
6. click on Ip Arress Tap
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8926d4b1-be86-4243-bfd5-feb4089227f7" />
7. defalte subnet as is it
   
9. Click **Add Subnet**

10. Subnet Purpose: **Azure Bastion**

11. Address Range: `10.0.1.0/24`

12. Click **Save**

13. Click **Review + Create**  
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/75498202-422a-45bb-82e4-088d084c0f5d" />

14. Click **Create**  
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a54eef3f-8c96-4008-84db-865c3628d348" />

# 🟩 Step 2 — Create Windows VM (Without Public IP)

1. Click **Virtual Machines**  
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)

2. Click **Create → Virtual Machine**  
   ![](https://github.com/user-attachments/assets/37cc27f8-d7af-4813-bc19-04d06f5373b9)

3. Resource Group: `Pratham`

4. VM Name: **VM**

5. Region: **Central India**  
  <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/474d0884-1fc0-404d-8953-67bd300df8c8" />

6. Choose Image: **Windows Server**

7. Choose Size  
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ac75eb19-3c9f-4980-a41d-a74c97bb389f" />

8. Username: `VM`

9. Password: `********`

10. Enable inbound port: **RDP (3389)**

11. Click **Next: Disk**  
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/2a83f5a9-4e1c-4dde-92f9-c38b1e11a0b7" />

12. Go to **Networking**  

13. Select Virtual Network: **Vnet**

14. Subnet: **Default**

15. Public IP: **None**

16. Click **Review + Create**  
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c66d4e85-a237-4729-bd38-5ae2f278752c" />

17. Click **Create**  
    <img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/55b62440-f4f5-41bd-bbac-37c9f62f1bf4" />

---

# 🟩 Step 3 — Create NSG (Internet BLOCK RULE)

1. Click **Virtual Machines**  
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)

2. Click On VM
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/7adf5c07-f819-430f-a795-0a5aa5aaaf23" />
3. Click on Networking Setting
4. click create port rule
5. click on outbount port rule
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ceb80f2f-cfb6-4000-8912-206e669680c2" />
6. Add Outbount Security Role
   1. source: `Any`
   2. source port range: `*`
   3. Distination: `any`
   4. service: `custom`
   5. Destination port range: `*`
   7. protocal: `any`
   8. action: `Deny`
   9. priority: `100`
   10. name: `Deny-Internet`
7. click add
  <img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/69082e3e-b6e6-4298-8c2c-47f2e7727f78" />
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6260dd8c-13e9-46a7-949c-8ab6325e4b1d" />
# 🟩 Step 4 - Connect to VM Bastion
1. Click **Virtual Machines**  
   ![](https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c)
2. Click On VM
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/7adf5c07-f819-430f-a795-0a5aa5aaaf23" />
3. click on connect
4. click on connect via bastion
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a006d4f5-d217-4501-b902-19b7b16f4a50" />
5. type username: `vm`
6. type password: `*******`
7. click conect
8. <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/f8a71bf1-d7eb-4f68-9ee1-1e7ed2935b77" />



# 🟩 Step 5 - Verify Internat Connection
1. click on microsoft edge
<img width="1918" height="1064" alt="image" src="https://github.com/user-attachments/assets/190c063a-ffdb-4fe4-a957-07ae82a51763" />
2. you can serch any website its not working
   <img width="1914" height="945" alt="image" src="https://github.com/user-attachments/assets/2f606655-67d0-4ea7-b3a8-a419635a4193" />
