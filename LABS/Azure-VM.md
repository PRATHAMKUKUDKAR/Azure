# 🖥️ Step 1 — Create Virtual Machine in Azure

This section explains how to create a Windows Virtual Machine in Azure with screenshots.

---

<img width="1597" height="788" alt="image" src="https://github.com/user-attachments/assets/69a49f09-5dda-47ea-9f65-725035b30066" />


## 1️⃣ Open Azure Portal
1. Go to **Azure Portal**
2. Sign in or create an account
3. Click on **Virtual Machines**
   ![](https://github.com/user-attachments/assets/de609490-7617-49c5-9b93-4621831af172.png)

---

## 2️⃣ Start VM Creation
4. Click **Create**
   ![](https://github.com/user-attachments/assets/1b1d9bce-1963-4c36-b076-90c2f6351863.png)

5. Select **Virtual Machine**
   ![](https://github.com/user-attachments/assets/afd4002b-045a-4ab4-8c45-8a48e92b4186.png)

---

## 3️⃣ Project Details
6. Fill project details:
   - **Resource Group:** Click *Create New*
   - Name: `PRATHAM`
   - Click **OK**

   ![](https://github.com/user-attachments/assets/38acb691-a194-4c97-bf96-eca4bf4875e8.png)

---

## 4️⃣ Instance Details
7. Configure VM:

| Setting | Value |
|--------|--------|
| Virtual Machine Name | `VM-1` |
| Region | Central India |
| Availability Zone | Zone 1 |
| Image | Windows Server 2025 *(or any OS as per requirement)* |
| Size | Standard_D2as_v5 (2 vCPUs, 8 GiB RAM) |
| Username | VM-1 |
| Password | ******** |
| Inbound Port | RDP (3389) |

![](https://github.com/user-attachments/assets/2d8358ea-40ec-45c2-be07-4a210d1f4b3d.png)  
![](https://github.com/user-attachments/assets/fe20a1bf-9073-4b6a-93f0-4416086586bb.png)

---

## 5️⃣ Networking Configuration
8. Open **Networking** tab

- Virtual Network → Auto-created (default)
- Subnet → Auto-created (default)
- Public IP → Auto-created (default)
- Click **Review + Create**

![](https://github.com/user-attachments/assets/869a2997-6638-45c9-b129-3ffde834a517.png)  
![](https://github.com/user-attachments/assets/dfe1b335-187e-4765-b834-e879aafa1ea1.png)

---

## 6️⃣ Create the VM
9. Click **Create**

![](https://github.com/user-attachments/assets/32e2aca3-900b-4887-add3-9f00b13dd120.png)

10. Deployment takes **2–3 minutes**
11. VM is successfully created

![](https://github.com/user-attachments/assets/f75b0566-7886-4c32-a7d5-9d1ecc249bd8.png)

---

### ✅ VM creation completed successfully!
