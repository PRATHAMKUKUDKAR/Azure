# Vnet Perring

<img width="944" height="534" alt="image" src="https://github.com/user-attachments/assets/8166c1cf-0fbc-4ca0-820d-d4349e2e1293" />

## Step 1 — Create First VNet (10 Network)

1. click on vertul network
<img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/5070d5db-15ac-4b9d-9fdf-136c17482378" />
2. click on create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3d97f97b-c931-4b5d-bce6-ff7f58014ade" />
3. select resouce group `pratham`
4. type vertual network name `vnet10`
5. select region `central india`
6. then click on ip address tap
<img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/250db680-c37f-43a4-9a7e-beec57567ccf" />
7. click on ad subnet
8. type ip range IP Range: `10.0.0.0/16`
9. type Subnet range: `10.0.1.0/24`
10. click on add
11. click on reviwe + create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/58f82d68-e732-48fd-baaa-9cd2be9bc676" />

## Step 2 — Create Second VNet (20 Network)
1. click on vertul network
<img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/5070d5db-15ac-4b9d-9fdf-136c17482378" />
2. click on create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3d97f97b-c931-4b5d-bce6-ff7f58014ade" />
3. select resouce group `pratham`
4. type vertual network name `vnet20`
5. select region `central india`
6. then click on ip address tap
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/488459a5-a442-4034-be3e-cd2e0845434e" />

7. click on ad subnet
8. type ip range IP Range: `20.0.0.0/16`
9. type Subnet range: `20.0.1.0/24`
10. click on add
11. click on reviwe + create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3a1a60ca-d31f-4788-bea9-a06aa27ed525" />

## Step 3 — Create Windows VM in Each VNet
1. click on vertual machin
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045" />
2. click on create
3. Click vertual machine
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b" />
4. select resource group `pratham`
5. type vertual machine name: `vnet10`
7. select Region: `central india`
8. select avability zone: `3`
<img width="1918" height="1073" alt="image" src="https://github.com/user-attachments/assets/d0690df8-aa05-4b59-b94f-0b365f379d7b" />

10. choice image : `window`
11. select size
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fa143b76-a451-4318-825d-491e1616c1d9" />
12. type username `vnet10`
13. type password `********`
14. select inbound role `RDP (3389)`
15. click next: disk
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/4c1667d7-431b-4bc7-95c8-b056671ae5a8" />
16. click on networking
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ca5fb417-e254-4641-8439-4410a0d36c9b" />
17. select vertual network: `vnet10`
18. click on Rewiev + create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/040a510e-4e2a-4deb-810e-588056561776" />
19. click on Create
<img width="1891" height="1071" alt="image" src="https://github.com/user-attachments/assets/0fa8fa8c-95e4-420d-bfe8-021a9f3eeb51" />
## Same for 2nd vm

## Step 3 — Create Windows VM in Each VNet
1. click on vertual machin
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045" />
2. click on create
3. Click vertual machine
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4124bd83-df56-4d1f-a741-13e9c769517b" />

4. select resource group `pratham`
5. type vertual machine name: `vnet20`
7. select Region: `central india`
8. select avability zone: `3`
<img width="1919" height="1067" alt="image" src="https://github.com/user-attachments/assets/60276263-76aa-452f-89b8-becdbc52be4f" />
10. choice image : `window`
11. select size
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fa143b76-a451-4318-825d-491e1616c1d9" />
12. type username `vnet20`
13. type password `********`
14. select inbound role `RDP (3389)`
15. click next: disk
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/064319fc-5cf5-479a-befd-c09d13b6c8aa" />

16. click on networking
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ca5fb417-e254-4641-8439-4410a0d36c9b" />
17. select vertual network: `vnet20`
18. click on Rewiev + create
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2397dfa8-9fa6-42e4-b2b5-78ac54e6bd3c" />
19. click on Create
<img width="1891" height="1071" alt="image" src="https://github.com/user-attachments/assets/0fa8fa8c-95e4-420d-bfe8-021a9f3eeb51" />

## Step 4 — Create VNet Peering
1. click on vertul network
<img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/5070d5db-15ac-4b9d-9fdf-136c17482378" />

2. click on vnet10
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/629eb2e4-056a-4e36-b3ee-eb67e74ade6c" />
3. click on setting
4. click on perring
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7545d226-4bea-4608-88dd-ef53ba1c9d29" />
5. click on add
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8b4c2735-dc3a-41f2-aafa-964b41afa874" />
6. type Peering name: `VNet10-to-VNet20`
7. Select Remote VNet: `VNet20`
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/18a3610d-ad14-44bd-8077-cc0f6b5dcc11" />
8. type local perring link name `VNet20-to-VNet10`
9. click on add
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1847f1ae-52cd-4681-8488-10e969bb4661" />

## stape 5 conect to remote desktop to both machine 
1. click on vertual machin
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/692d9f1a-ebd4-4398-990e-fac74ee47045" />
2. click on vnet10
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/275c9d05-39a1-4e00-a7d0-8000c4d5b057" />
3. click on connect
<img width="1893" height="1079" alt="image" src="https://github.com/user-attachments/assets/afedf0d9-b135-401e-8f56-13476210578b" />
4. copy public ip
5. click on serch bar
6. search remote desktop
7. click on remote desktop connection
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/acdb9bc0-eae4-4c7a-aa7d-d617a08aae5c" />
8. paste the public ip
9. click on connect
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fcc6906e-7193-44fe-842d-eeed28390217" />
10. type username
11. type password
12. click ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1735008d-12f8-46f6-8cf9-467c52e3a821" />
13. click on yes
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/082bd01f-65ea-4ff1-b9a7-635f9d4af62b" />

### same for vnet20

## stap 6 check machine ip And Disable firewall both machine
### Vnet10 machine
1. clickon serch bar
2. serch powersheel
3. click on window powershell 
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0407b1ee-091d-4bb2-b833-9b85b56d62b8" />
4. Type command
```
ipconfig
```
<img width="1920" height="1004" alt="image" src="https://github.com/user-attachments/assets/90313fe4-51a2-499c-8aa7-5fd52b6a973d" />

4. type this command
```
New-NetFirewallRule -DisplayName "Allow ICMPv4" -Protocol ICMPv4
```
<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/0f1bf8ef-fca2-49be-be44-6a6adb1f5565" />

### vnet20 machine 

1. clickon serch bar
2. serch powersheel
3. click on window powershell 
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5c0b1a4d-26f9-4f0a-8413-b20e2a252a80" />

4. Type command
```
ipconfig
```
<img width="1920" height="1015" alt="image" src="https://github.com/user-attachments/assets/2dd60770-a01f-4cab-9316-e5b9af8fa72b" />

5. type this command
```
New-NetFirewallRule -DisplayName "Allow ICMPv4" -Protocol ICMPv4
```
<img width="1920" height="1006" alt="image" src="https://github.com/user-attachments/assets/a94fb284-e20e-4202-b533-056fc7d2d5e9" />

## Stape 7 ping 

1. type comand
```
ping 20.0.2.4
```
<img width="1920" height="1011" alt="image" src="https://github.com/user-attachments/assets/a7487c71-183e-4e9e-8bf1-0eaad0546b2d" />
