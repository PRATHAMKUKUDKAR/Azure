# Azure Bastion

## Stape 1 create vnet
1. click vartual network
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9acbf209-4afd-4170-910a-63c82d3256e0" />
2. click on create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/bdfa34e6-7c5c-497b-89ea-69a505b49973" />

3. Type Resource Group: `Pratham`
4. type VNet name: `Bastion-vnet`
5. type Region: Central India
6. click on IP Adresss
<img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/094036cf-6d5e-4d12-b23d-5f2161ae431e" />
7. click on Add subnet
8. Select Subnet Purpose: `Azure Bastion`
9. type Address range: `40.0.1.0/24`
10. click on Save
11. click on rewiev + create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5d27c551-a8d8-4884-80db-03f0b98cf2da" />

12. click on Create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ed1f32b6-355f-4d16-b4d1-d761665b74ac" />

## Stape 2 create vm
1. click on Vertual machine
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c" />
2. click on create
3. click on vertual machine
<img width="1911" height="1056" alt="image" src="https://github.com/user-attachments/assets/37cc27f8-d7af-4813-bc19-04d06f5373b9" />
4. select Resource Group `Pratham`
5. type vertual machine name: `Basion-VM`
6. Select Region: `Cental India`
<img width="1919" height="1074" alt="image" src="https://github.com/user-attachments/assets/15b506ed-e143-4ba8-96dc-538a9ce11c32" />
7. choice image: `window server`
8. choise size
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9015c3c3-e011-4e21-98a8-3c8e84f189b9" />
9. type username: `Bastion-VM`
10. type Password: `********`
11. select inbound port : `RDP (3389)`
12. click Next:Disk
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1fd9a948-e8fd-4d11-8e52-5fb3885e6aee" />
13. click on Networking
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a11a6227-d7bd-4c45-b0f2-ac6a0e038fed" />
14. Select vertual Network: `Basion-Vnet`
15. Select Subnet: `Defalte`
16. Select Public IP: `None`
17. click Reviw + Create
<img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/7deccdb2-1d1b-4cd8-902b-281fc4aa9c09" />
18. click Create
<img width="1912" height="1078" alt="image" src="https://github.com/user-attachments/assets/1f5450fd-d656-409d-81fd-248357486f31" />

## Stape 3 create Bastion 
1. open serchbar and serch Bastion
2. click on Bastions
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/127d990c-5c5a-4e3a-a04e-28008eb1d5cc" />
3.click on Create
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/8dde39ad-a561-4522-a581-e71acc857a9c" />
4. Selct Resource Grup: `Pratham`
4. type bastion Name: `Bastion`
5. select Region: `Central India`
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d38caffc-97a9-478e-ae7d-e195e4efa523" />
7. select Vertual Network: `Basion-Vnet`
8. select Public Ip Adrres: `Create New`
9. Click Rewiv +Create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3e2a5763-84d1-4d1c-a959-654b27f51394" />
10. Click on Create
<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/4b9ba38a-fd4e-45d8-b836-12350cc26f01" />

## Stape 4 Connect Vm to Bastion
1. click on Vertual machine
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f3f5d080-900d-4233-9a98-ed798b41fe8c" />
2. click on Basion-VM
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b72fc8e0-7e34-425b-b9e6-24a13689e0a8" />
3. click onConnect
4. Click on Connect via Bastion
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/18015234-7438-4ed9-92e3-54d7017831ae" />
5. Type UserName: `Bastion-VM`
6. type Password: `*********`
7. click Connect
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7597edbb-a892-4d69-8016-a198183ff111" />
9. Now you can see conected
<img width="1919" height="949" alt="image" src="https://github.com/user-attachments/assets/ab509358-125a-4397-8a3b-6825f55f3ec3" />
