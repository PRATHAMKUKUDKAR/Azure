# site to site vpn connection

## stape 1  create vnet and subnet 
1. click on vertual network icone
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2dcf4737-eeef-4f7b-a937-384088b47e7c" />
2. click on create
   <img width="1919" height="1072" alt="image" src="https://github.com/user-attachments/assets/0bc6c4c7-6125-4c83-ac9e-ef2ed43b3b12" />
3. Select resource group : `PRATHAM`
4. TYPE VERTUAL NETWORK NAME : `V-NET`
5. SELECT REGION : `CENTRAL INDIA`
6. CLICK ON IP ADRRESS
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/df530974-4075-4218-93af-283e90dd3c5c" />
### CREATE 2 SUBNET
#### SUBNET 1 FOR VM
8. CLICK ON ADD SUBNET
9. SELECT SUBNET PURPOSE : `DEFALTE`
10. TYPE NAME : VM-SUB
11. TYPE STARTING ADDRESS: `10.0.1.0`
12. SELECT SIZE `/24`
13. CLICK ON ADD
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/31cfd727-1b38-4d56-98e5-e3b9ff1b0543" />

### SUBNET 2 FOR VERTUAL NETWORK GATEWAY
8. CLICK ON ADD SUBNET
9. SELECT SUBNET PURPOSE : `VERTUAL NETWORK GATWAY`
10. TYPE NAME : `GATWAYSUBNET`
11. TYPE STARTING ADDRESS: `10.0.2.0`
12. SELECT SIZE `/24`
13. CLICK ON ADD
14. CLICK ON REWEW + CREATE
    <img width="1915" height="1075" alt="image" src="https://github.com/user-attachments/assets/b36a5f7e-ca74-45f9-adaa-4984f55a1706" />
15. CLICK 0N CREATE
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/30f46b6f-9967-4384-b3c9-ac4aebb18bc6" />

## stape 2 CREATE VM 
1. CLICK ON VERTUAL MACHINE ICONE
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fd0a190b-138d-4b66-b1e4-c92879221440" />
2. CLICK ON CREATE
3. CLICK ON VERTUAL MACHINE
   <img width="1917" height="1074" alt="image" src="https://github.com/user-attachments/assets/1f4b89f9-d058-4b02-87a4-edf2ffba454b" />
4. selct resource group : `PRATHAM`  ------------------------------------ (Any image you can choice your own choince)
5. Type vertual machine name : `VM-1`  ------------------------------------ (Any image you can choice your own choince)
6. SELCT REGION : `Central India`
7. Avability zone : `1`
8. select image : `window server` ------------------------------------ (Any image you can choice your own choince)
9. Select size : `Standard_D2as_v5 - 2 vcpus, 8 GiB memory`       --------------------- (any size you can choice your own choice)
10. type username : `VM-1`
11. type password : `********`
12. conform Password: `******`
13. select nbound port : `3389`   ---------------------------------( your image depended port)
14. click on next
    <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/c36586f6-ff1e-4e6c-ac15-ac091d5b93a9" />
    <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/e3c34404-e6de-49ad-a725-20a906edb901" />
    <img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/8f03cf97-6d4a-4d2b-984f-3513396a4ca9" />

15. go to networking tab
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c49423b6-b6a5-49d9-b200-159d82dec072" />
16. select vertual network : `V-NET` -----------------------(you can create alredy choise them)
17. select subnet : `VM-SUB`          -----------------------(you can create alredy choise them for vm subnet)
18. click on rewev + create
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b489d514-50db-4ae7-bf6e-0d84c035689c" />
19. click on create
    <img width="1918" height="1077" alt="image" src="https://github.com/user-attachments/assets/63d52036-c311-46d2-9092-6605c9e41566" />
### SECURITY GROUP
1. CLICK ON VM
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c0837a10-d834-470f-a3d8-48e9d609b70c" />
2. GO TO NETWORKING
3. CLICK ON NETWORK SETTING
4. CLICK ON CREATE PORT RULE
5. CLICK ON INBOUND PORT RULE
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b5948280-c155-40cc-b231-6f15ef8304bf" />
6. SORCE : `ANY`
7. SORCE PORT RANGES: `*`
8. DESTINATION : `ANY`
9. SERVICE : `HTTP`
10. Destination port ranges: `80`
11. PROTOCAL : `TCP`
12. PRIVORITY: `20`
13. NAME: `HTTP`
14. CLICK ON ADD
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6b075b29-4e32-4f5c-99ff-0d41f5cf648a" />

### CONNECT TO MACHINE 
1. GO TO VM
2. CLICK ON CONNECT
3. COPY PUBLIC IP
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/e96883d2-6192-4d4c-87c7-62eecdd8a007" />
4. CLICK ON YOUR COMPUTER WINDOW ICONE SERCH REMOTE DESKTOP
5. CLICK ON REMOTE DEESTOP CONECTION
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/54901e48-daf7-440f-8a69-a8d2b2465720" />
6. COPUTER : `40.81.227.210`               --------------------------------( PASTE YOUR VM PUBLIC IP HERE )
7. CLICK ON CONNECT
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8a4d9413-7ab5-4902-941a-1dac9d5be47c" />
8. user name: `VM-1`  ------------------------------------- (type youre vertual machine username)
9. password: `*****` ---------------------------------------(type youre vartual machine password)
10. click on ok
    <img width="1919" height="1074" alt="image" src="https://github.com/user-attachments/assets/27ccfecd-c091-49f2-832e-f0ce4d7c4760" />
11. click on yes
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/372c55d1-95da-408a-b8cd-31f58a69d931" />
### Firewall of 
**this is not best way to of firewall**
**this way only for practic purpose**
1. press wendow+R buton in keybord
2. type firewall.cpl
3. click on ok
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f98bb8dd-2dd7-4686-aefe-cb3b1dbb2bf1" />
4. click on trun window defendaf firewall on or of
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6366a21c-025e-4719-a0f5-15d854307148" />
5. private network setting
   click on trun of window defendaf firewall
6. public network setting
   click on tun of eindow defender firewall
7. click on ok
<img width="1918" height="1074" alt="image" src="https://github.com/user-attachments/assets/2ebbb8f5-1d7e-4cb1-ad73-e496b5d38cfb" />


## stape 3 create vertual network Geteway
1. click on serch tap
2. then serch vng
3. click  on Vertual Network Gateway Icone
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7a699b9b-ea5c-4fad-adc2-106169e80b1b" />
4. click on create
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/40c8bde5-c645-46f6-9430-e9a7d0a618c9" />
5. SELECT RESOURCE GROUP : `PRATHAM`
6. TYPE NAME : `VNG`
7. SELECT REGION : `CETRAL INDIYA`
8. SELECT GATEWAY TYPE : `VPN`
9. SELECT VERTUAL NETWORK : `V-NET`  -------------------------------- (YOU CAN ALLREADY CREATED) 
10. SELECT SUBNET : `GATEWAYSUBNET`  ----------------------------------( YOU CAN ALREADY CREATED CHOICE THEM)
11. SELECT PUBLIC IP ADDRESS : ` CREATE NEW`
12. TYPE PUBLIC IP ADRRESS NAME : `VNG-PUB-IP`
13. ENABLE ACTIVE ACTIVE MODE : `DISABALE`
14. CONFIGURE BGP : `DISABLE`
15. CLICK ON REWEV + CREATE
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c4729370-e52a-4408-ac11-91e16248fbe8" />
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/903ed485-a74a-4aea-8efa-2791910e5807" />

## Stap 4 VPC CONFIGURATION IN AWS (USE BY DEFALTE VPC)
### CREATE VERTUAL PRIVATE GETWAY IN AWS
1. go to aws console
2. search vpc
3. click on vpc
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/6fd5be68-4138-4ffa-bbc4-a484da2df406" />
4. croll down and click vertual private gateway
5. click on create vertual private gateway
   <img width="1919" height="1065" alt="image" src="https://github.com/user-attachments/assets/514265da-29cf-4097-a4d8-4a2738deb3b3" />
6. TYPE NAME: `VPG`
7. CLICK ON CREATE VERTUAL PRIVATE GATEWAY
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2255cd86-7953-4125-a262-52c6eef13617" />
8. SELECT VPG
9. CLICK ON ACTION
10. CLICK ON ATTACH TO VPC
    <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/5b15fd7c-3750-49d3-a686-5573daec68b8" />
11. SELECT BY VPC ---------------------------------(BY DEFALTE VPC)
12. CLICK ATTACH TO VPC
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5738b384-7ece-4ed4-8fd9-ecc379556dc5" />
### CREATE CUSTOMER GATEWAY IN AWS
1. CLICK ON CUSTOMER GATEWAY
2. CLICK ON CREATE CUSTOMER GATEWAY
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/83482745-13dd-4d46-84d9-26cc4901f3de" />
3. TYPE NAME : `AZURE-CGW-TO-AWS`
4. TYPE IP : `4.224.72.113`   -----------------------------(COPY VNG PUBLIC IP IN AZURE)
5. CLICK ON CREATE CUSTOMER GATEWAY
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8965b5ba-393f-4cc5-80b3-ffb62f50693a" />
### Site-to-Site VPN connections IN AWS
1. CLICK ON SITE TO SITE VPN CONECTION
2. CLICK ON CREATE VPN CONNECTION
   <img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/aeec08c5-f3d0-411a-a766-6704e74c842c" />
3. TYPE NAME: `VPN`
4. SELECT TARGET GATEWAY TYPE: `VERTUAL PRIVATE GATWAY`
5. SELECT VERTUAL PRIVATE GATEWAY: `VPG`      ------------------------------(YOU CAN CREATED ALREDY )
6. SELECT CUSTOMER GATEEWAY: `AZURE-CGW-TO-AWS` ----------------------------(YOU CAN CREATED ALREADY)
7. SELECT ROUTING OPTION : `STATIC`
8. TYPE STATIC IP PRIFIX: `10.0.0.0/16`
9. CLICK ON CREATE VPN CONNECTION
   <img width="1919" height="1069" alt="image" src="https://github.com/user-attachments/assets/010f4599-d40a-4370-ab8e-4f87bd5620a3" />
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fa658c61-84db-47d3-8f64-c4712a0a7d49" />


### ADD ROUTE IN DEFALTE ROUTE TABLE IN AWS
1. CLICK ON ROUTE TABLE
2. CLICK ON EDIT ROUTE
   <img width="1919" height="1072" alt="image" src="https://github.com/user-attachments/assets/ce4b217e-39eb-4222-893b-cd9dad2298d3" />
3. CLICK ON ADD ROUTE
4. TYPE DESTINATION: `10.0.0.0/16`
5. SELECT TARGET: `VERTUAL PRIVATE GATEWAY` `SELECT VERTUAL PRIVATE GATWAY ID`
6. CLICK ON SAVE CHENGES
   <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/4eb728c2-d44f-44fe-83ce-db588544e15b" />


### create ec2 In AWS
1. serch ec2
2. click on ec2
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/70f81f71-b152-4b00-8703-10f468453561" />
3. click on lunch instance
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/da9a6fc6-62b8-449c-aa30-ef853730e9a4" />
4. TYPE NAME: `MACHINE1`
5. SELECT APPKICATION AND OS IMAGE: `AMAZONE LINUX`
6. SELECT INSTANCE TYPE : `T3MICRO`
7. SELECT KEY PAIR : `LONDON`  -----------------------------(YOU CAN CREATE NEW KEY PAIR AND CHOICE THEM)
8. SELCT NETWORK: `CHOICE FEFALTE VPC`
9. FIREWALL SECURITY GROUP
10. ALLOW SSH TRAFIC
11. CLICK ON LANCH INSTANCE
    <img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/96437547-67fa-4cbd-82ca-38adfc0eedce" />
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/495860bb-4135-42a7-be90-236fb9451fce" />
   <img width="1919" height="1075" alt="image" src="https://github.com/user-attachments/assets/2a782772-e17a-4f0c-8969-4f202044ff46" />

### ALLOW SECURITY GROUP
1. SELECT ON MACHINE1
2. GO TO SECURITY TAP
3. CLICK ON SECURITY GROUP
   <img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/e1d90d64-6e1a-44d3-8bf9-54e9b08d73d7" />
4. click on edit inbound rule
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4f9d3c70-b3e1-4726-87c7-7187147bb83f" />
5. click on add
6. select type: `all trafic`
7. source: `anywhere`
8. click on save rule
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a4e14443-739e-4345-b12f-3e2eb17df20e" />
### connect to ec2
1. select machine1
2. click on connect
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/189cc13a-1880-494a-aee9-fccb6523edcd" />
3. click on again connect
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/69fb46b5-ebe6-4687-9bea-0957f6b22c76" />


## STAP 5 CREATE LOCal NETWORK GATEWAY IN AZURE
1. SERCH LNG
2. CLICK ON LNG ICONE
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/14aad5fe-827c-4e28-be98-dff5b707d676" />
4. CLICK ON CREATE
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a64dc2d8-90fb-4336-9c88-d1992c807718" />
4. SELECT RESOURCE GROUP: `PRATHAM`
5. SELECT REGION: `CENTRAL INDIA`
6. TYPE NAME: `LNG`
7. TYPE IP ADDRESS: `3.8.76.122` ---------------------------------- (THIS IP IS AWS SITE TO SITE CONNECTION TUNAL 1 OUTSIDE IP) 
8. TYPE ADDRESS SPACE: `172.31.0.0/16`------------------------------(THIS ADDRESS SPEACE IS AWS VPC CIDR)
9. CLICK ON REWEV+CREATE
10. CLICK ON CREATE
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fc604513-5a8d-4dee-97c9-ca9c6339fb11" />
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b9a1c48d-ebec-4e52-be77-ce19a3f59cbb" />

## STAPE 6 CREATE VNG CONECTION IN AZURE
1. GO TO VNG
2. CLICK ON VNG --------------------------- ( YOU CREATED ALREDY )
3. CLICK ON CONNECTION
4. CLICK ON ADD
   <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/71ad0d95-a46a-4742-b4d8-fd90057e52ba" />
5. SELECT RESOURCE GROUP: `PRATHAM`
6. SELECT CONNECTION TYPE : `SITE TO SITE`
7. NAME : `VNG-CONNECCTION`
8. SELECT REGION : `CENTRAL INDIYA`
9. CLICK ON NEXT:SETTING
    <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/e14ed389-32eb-4adf-ae1d-5b978c798545" />
10. SELECT VERTUAL NETWORK GATEWAY: `VNG`    ----------------------(YOU CAN CREATED ALREDY )
11. SELECT LOCAL NATWORK GATEWAY: `LNG`        ----------------------(YOU CAN CREATED ALREDY )
12. CHOICE ATHENTICATION METHOD: `SHARED KEY`
13. SHYERD KEY: `****************`             -----------(THIS SHAREED KEY FIND IN AWS TUNAL -- CLICK ON VPN CONNECTION--CLICK ON ACTION--CLICK ON MODIFY VPN TUNAL OPTION--THEN SELECT TUNAL 1---COPY PRE SHARED KEY)
14. CHOICE IPSEC/IKE POLICY : `CUSTOME`
15. IKE PHASE1: `MATCH WITH AWS TUNAL PHASE1`
16. IKE PHASE2: `MATCH WITH AWS TUNAL PHASE2`
17. CLICK ON NEXT
    <img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/ef8bd6bb-314a-45c0-86cd-03bb435541aa" />
    <img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/1aa6c27b-55dd-4f34-bdf4-9f784444076a" />
18. CLICK ON REWEW+CREATE
19. CLICK ON CREATE
    <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4ccefe73-6a76-4cd6-94e0-645078f6187c" />



## stap 7 texting
1. conect to ec2
2. and type `ping 10.0.1.4` -----------------------------------------(this private ip copy form vm-1)
   <img width="1919" height="1033" alt="image" src="https://github.com/user-attachments/assets/0ac8a7a3-6ddf-4262-af23-8c447a283ce4" />
this is susses site to site vpn 
