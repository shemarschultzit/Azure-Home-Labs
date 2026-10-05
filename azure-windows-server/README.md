# Azure Windows Server Virtual Machine Lab

## Objective

The objective of this lab was to deploy and administer a Windows Server virtual machine in Microsoft Azure, connect it to an existing virtual network, securely access it using Remote Desktop, verify network configuration, install a server role, and properly clean up resources after use.

## Technologies Used

- Microsoft Azure
- Azure Virtual Machines
- Windows Server 2025
- Azure Virtual Network
- Azure Network Security Groups
- Remote Desktop Protocol (RDP)
- Windows Server Manager
- PowerShell
- Internet Information Services (IIS)
- GitHub

## Lab Environment

- Resource Group: `rg-networking-homelab`
- Virtual Machine: `vm-winserver01`
- Computer Name: `WIN-SRV01`
- Operating System: Windows Server 2025 Datacenter: Azure Edition
- VM Size: `Standard_D2as_v4`
- Virtual Network: `vnet-homelab`
- Subnet: `snet-servers`
- Server Subnet Range: `10.10.1.0/24`
- Network Security Group: `nsg-servers`

## Implementation

### 1. Deployed the Windows Server Virtual Machine

Created an Azure virtual machine named `vm-winserver01` using Windows Server 2025 Datacenter: Azure Edition.

The VM was deployed with the `Standard_D2as_v4` size.

### 2. Connected the VM to the Existing Network

Placed the VM inside the existing Azure networking environment:

- Virtual Network: `vnet-homelab`
- Subnet: `snet-servers`
- Subnet Range: `10.10.1.0/24`

The existing subnet-level Network Security Group, `nsg-servers`, continued to control inbound traffic.

### 3. Configured Temporary RDP Access

Created a temporary inbound NSG rule allowing TCP port `3389` only from my current public IP address.

This allowed secure Remote Desktop access without exposing RDP to the entire internet.

### 4. Connected to Windows Server with RDP

Connected to the Windows Server VM using Remote Desktop and the administrator account created during deployment.

### 5. Renamed the Server

Renamed the Windows Server computer to:

`WIN-SRV01`

The server was restarted to apply the hostname change.

### 6. Verified the Network Configuration

Used PowerShell commands including:

```powershell
hostname
ipconfig


