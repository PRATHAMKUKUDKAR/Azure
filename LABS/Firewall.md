# 🚀 **STEP 1 — Create VNet

1. Click **Virtual Network**
   ![](https://github.com/user-attachments/assets/2cc987c7-e66b-4248-b097-698dbcd1b1b8)

2. Click **Create**
   ![](https://github.com/user-attachments/assets/b5540a1c-667d-40a2-8b2b-4dcd1c7fa12a)

3. Select Resource Group: `pratham`

4. VNet Name: **VNET**

5. Region: **Central India**

6. Go to **IP Addresses** tab
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/591b61d7-7d1f-4aeb-bfcf-0a7c0d1d2be4" />

7. Click **Add Subnet**
8. CLICK ON EDIT ICONE
9. TYPE SUBNET NAME: `SUBNET1`
8. IP Range: `10.0.0.0/16`
9. Subnet Range: `10.0.1.0/24`
10. Click **SAVE**
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7cfd3e86-82af-4850-92e5-97cf242380ea" />
11. CLICK ON ADD SUBNET
12. SELECT SUBNET PURPOSE: `AZURE FIREWALL`
13. NAME: `AzureFirewallSubnet`
14. IP Range: `10.0.0.0/16`
15. Subnet Range: `10.0.2.0/24`
16. Click **Add**
17. Click **Review + Create**
   <img width="1919" height="1072" alt="image" src="https://github.com/user-attachments/assets/c4e0d770-b1ae-4918-9549-71c689511059" />
18. click on Create
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/7d424c66-3279-4bf3-b98b-2020625e1ffa" />




# 💻 **STEP 3 — Create VM **

1. Click **Virtual Machines**
   ![](https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045)

2. Click **Create → Virtual Machine**
   ![](https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b)

3. Resource Group: `pratham`

4. VM Name: **VM**

5. Region: **Central India**

6. Availability Zone: **3**
  <img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/ff25d1ae-4543-48f2-a766-91e25a16c7e0" />


7. Image: **Windows Server**

8. Select Size
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/eeaa1131-8132-493a-b8bd-58d6679396bc" />


9. Username: `VM`

10. Password: ******

11. Enable **RDP (3389)**

12. Disk → Next
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8e37feff-a0da-4904-9b8a-8ebd80ddf378" />


13. Networking →
14. Select VERTUAL NetWORK: **VNET**
15. SELECT SUBNET: **SUBNET1**
17. Review + Create
    <img width="1919" height="1071" alt="image" src="https://github.com/user-attachments/assets/540bc0c0-0852-4eb3-a184-6b4375c2297a" />

15. Click **Create**
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b15c5f29-c5ef-45f7-b0ec-f01ef85e128f" />

---




# 💻 **STEP 4 — Create FIREWALL **

1. CLICK ON SERCH BAR SERCH FIREWALL
2. CLICK ON FIREWALL ICONE
<img width="1919" height="1071" alt="image" src="https://github.com/user-attachments/assets/7e837283-14bc-4d87-bb21-c580b0f1d318" />
3. CLICK ON CREATE
<img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/1f6ce662-20a5-4fb6-a80a-dcb6f1051f7f" />
4. SELECT RESOURCE GROUP: `Pratham`
5. TYPE NAME: `FIREWALL`
6. SELECT REGION: `CENTRAL INDIA`
7. SELECT FIREWALL SKU: `STANDARD`
<img width="1919" height="1058" alt="image" src="https://github.com/user-attachments/assets/fb03804a-987a-4c0c-8e52-bbe8f19cb1bb" />
8. SELECT Firewall management: `Use Firewall rules (classic) to manage this firewall`
9. Choose a virtual network: `Use existing`
10. SELECT VIRTUAL NETWORK: `VNET`
11. PUBLICK IP ADRESS: CLICK ON ADD NEW
12. NAME `FIREWALL-IP-PUB`
13. CLICK ON OK
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/eb37ca82-2167-436b-8049-ca8561aeae3e" />
14.Enable Firewall Management NIC: `UNTICK ON CHEK BOX`
15. CLICK NEXT:TAGS
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fae1e142-148f-4bc5-9ff1-7f02c7c458f9" />
16. CLICK REWIEV + CREATE 
17. CLICK ON CREATE
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/989a68ff-2e9c-4e98-b323-c5b2381860a9" />



# 💻 **STEP 5 — Create NATROLE CONNECTION FOR RDP **
1. CLICK ON gO TO RESORCESS
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6203e735-d8e4-4b01-bdf3-d4e8d895b620" />
2. CLICK ON SETTING
3. CLICK ON RULES (CLASIC)
4. CLICK ON Add NAT rule collection
<img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/a96e4b8e-c639-4d4d-bf89-1557717ed8b7" />
5. TYPE NAME: `DNAT`
6. TYPE PRIORITY `ANY YOU WANT`
7. NAME: `RDP`
8. PROTOCAL: `TCP`
9. SOURCE TYPE: `*` // * MIANCE ANY IP ADRRESS
10. DESTINATION ADDRESS: `FIREWALL PUBLIC IP`
11. DESTINATION PORT: `3389`   //3389 MEANCE RDP PORT
12. Translated address: `VM PRIVATE IP`
13. TRANSLATED PORT: `3389`
14. CLICK ADD
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/eb4e278e-368d-40f1-899d-c4b55c7269cd" />

15. NOW YOU CAN LOGIN ANY COMPUTER

### VERIFY
1. CLICK ON WINDOW ICONE
2. SERCH REMOTE
3. CLICK REMOTE DESKTOP CONECTION
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/e57bc33b-a42b-4321-95e9-2f625e00e74a" />
 4. COPY FIREWALL PUBLIC IP
 5. PASTE IT COMPURE OPTION 
 6. CLICK ON CONNECT
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/704fee5d-16ed-4413-b807-211a1d3eac63" />
7. type username of VM
8. type passwor
9. click on ok
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/07b1262d-3cd2-4b1c-8e0f-52daacdacf59" />
10. now its connect successfuly
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a8541fbb-cfc5-404f-a17b-ad12530f02d9" />


# 💻 **STEP 5 — Create NATROLE CONNECTION FOR RDP **
