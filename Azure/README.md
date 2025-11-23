# Cloud_Module_Week_9
## Assignment: Set Up an Azure Virtual Machine with a Free Account

**Student:** Gamzenur Uzunlu  
**Course:** VIT-9 / Week-9 (Cloud Computing / Azure Fundamentals)  
**Date:** 23/11/2025  

---

## Objective
The purpose of this assignment is to provide hands-on experience in creating, configuring, and managing virtual machines on Microsoft Azure. Students learn essential cloud computing skills including compute, storage, networking, and database management.

---

## Assignment Steps

### 1. Create an Azure Account
- Sign up for a free Azure trial account (student benefits can be utilized).
- Activate a Pay-As-You-Go subscription if necessary.

### 2. Create a Resource Group
- Navigate to **Resource Groups** in the Azure portal.
- Create a new resource group named `GamzenurUzunlu_RG`.
- Select a region (e.g., *West Europe*) for deployment.

---

### 3. Create a Virtual Machine
- Go to **Virtual Machines** in the Azure portal and create a new VM.
- **Basic Settings**:
  - Resource group: `GamzenurUzunlu_RG`
  - VM name: `GamzenurUzunluVM`
  - Region: Same as resource group
  - Image: Windows Server 2019 Datacenter / Ubuntu Server 20.04 LTS
  - Size: `Standard_B1s` / `Standard_B2s` (depending on free credits)
  - Administrator username and strong password

- **Disks**: Default settings; Premium SSD recommended for OS disk.
- **Networking**: Default VNet & subnet, assign public IP, allow RDP/SSH.
- **Management**: Configure monitoring and diagnostics.
- **Advanced & Tags**: Optional extensions and tags (e.g., "GamzenurUzunlu", "Assignment").

**Review & Create** the VM.

---

### 4. Connect to the Virtual Machine
- **Windows**: Download the RDP file via **Connect** in Azure portal, login with admin credentials.  
  ![Access through RDP](Azure/Access_through_RDP.png)
- **Linux**: Connect via SSH using public IP.

---

### 5. Create and Connect to Azure File Share
- Navigate to **Storage Accounts** → create a storage account.
- Within storage account, create a **File Share**.
- Mount file share on VM & local PC.
  - Windows: Map network drive  
    ![File Share on VM](Azure/File_share_on_VM.png)  
  - Test file operations (create, read, delete)  
    ![File Share Read & Write](Azure/File_share_read&write.png)

---

### 6. Tasks on the Virtual Machine (Optional)
- **Windows VM**:
  - Install IIS Web Server & publish a website  
    ![IIS Website](Azure/IIS_Website.png)
  - Install SQL Server Express & create a database  
    ![SQL Database](Azure/Create_SQL_Database.png)
- **Linux VM**:
  - Install Apache & MySQL
  - Configure Samba file sharing
  - Test file operations on Azure File Share

---

### 7. Resource Group & Server Management
- Overview of deployed resources and Server Manager  
  ![Resource Group](Azure/Resource.png)  
  ![Server Manager](Azure/Server_Manager.png)

---

## Challenges Solved
- **RDP Black Screen & Protocol Errors**: Resolved using Azure Serial Console and service restart.
- **SQL Server Silent Installation**: Configured correct parameters, firewall, and SQL Browser.
- **Azure File Share Mounting**: Mapped via CLI, resolved auth issues.
- **IIS Deployment**: Enabled features, verified public IP connectivity.

---

## Learnings
- Hands-on experience with Azure core services: VMs, Resource Groups, Storage Accounts, File Shares.
- Troubleshooting VM access using Serial Console.
- Installing and configuring Windows Server components using PowerShell/CMD.
- Deploying a website on IIS and creating SQL databases.
- End-to-end cloud deployment covering compute, storage, networking, web hosting, and database layers.

---

**Note:**  
After assignment completion, remember to **delete all resources** to avoid additional charges.  

This project demonstrates practical cloud computing fundamentals and strengthens professional Azure skills.
