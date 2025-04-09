<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

## 🛠️ Step 1: Connect to Your VM via RDP

1. In Azure Portal, go to your VM
2. Click **Connect → RDP**
3. Download the RDP file and log in with the local admin account

---

## 📦 Step 2: Install Active Directory Domain Services (AD DS)

1. Open **Server Manager**
2. Click **Add roles and features**
3. Choose **Role-based or feature-based installation**
4. Select your local server
5. Under **Server Roles**, check **Active Directory Domain Services**
6. Accept the required features → Click **Next** → **Install**

---

## 🏁 Step 3: Promote the Server to a Domain Controller

After installation:

1. Click the **flag icon** in Server Manager (notification bar)
2. Select **Promote this server to a domain controller**
3. Choose **Add a new forest**
    - Enter your **Root domain name** (e.g., `mydomain.local`)
4. Set the **Directory Services Restore Mode (DSRM) password**
5. Click **Next** through all steps → **Install**

VM will reboot after promotion.

---

## 🌐 Step 4: Configure DNS (if needed)

1. After reboot, log in using your domain admin account
2. Verify DNS installation under Server Manager
3. Add Forwarders (e.g., 8.8.8.8 or your ISP's DNS)

---

## 🧑‍💼 Step 5: Create Organizational Units and Users

1. Open **Active Directory Users and Computers**
2. Create OUs:
   - Right-click domain → New → Organizational Unit
3. Add new users:
   - Right-click an OU → New → User

---

## 🖥️ Step 6: Join Additional VMs to the Domain

On a second VM:

1. Set static IP and DNS to point to domain controller
2. Right-click **This PC → Properties → Change Settings**
3. Click **Change** next to computer name
4. Choose **Domain** → Enter domain name (e.g., `mydomain.local`)
5. Provide domain admin credentials → Restart the VM

---

## 🛡️ Optional: Install Group Policy Management

1. Open **Server Manager → Add roles and features**
2. Under **Features**, select **Group Policy Management**
3. Use it to create and manage GPOs for the domain

---

## ✅ Summary

You now have:
- A working AD Domain Controller in Azure
- The ability to manage users, groups, and security policies
- Optional GPO management
