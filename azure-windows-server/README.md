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
