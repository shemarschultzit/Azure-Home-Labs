# Azure Role-Based Access Control (RBAC) Lab

## Objective

The objective of this lab was to gain hands-on experience with Microsoft Azure Role-Based Access Control (RBAC) by creating a resource group, deploying a user-assigned managed identity, and assigning least-privilege access at the resource-group scope.

## Technologies Used

- Microsoft Azure
- Azure Resource Groups
- Azure Role-Based Access Control (RBAC)
- Azure Managed Identities
- Azure Activity Log
- GitHub

## Lab Environment

- Resource Group: `rg-contoso-it-lab`
- Managed Identity: `id-rbac-homelab`
- RBAC Role: `Reader`
- Scope: Resource Group

## Implementation

### 1. Created the Resource Group

Created a dedicated Azure resource group named `rg-contoso-it-lab` to provide an isolated scope for the RBAC lab resources.

### 2. Created a User-Assigned Managed Identity

Created a user-assigned managed identity named `id-rbac-homelab`.

The managed identity was used as the security principal for testing Azure role assignments without requiring an additional Microsoft Entra user account.

### 3. Assigned the Reader Role

Opened **Access Control (IAM)** on the resource group and assigned the built-in `Reader` role to `id-rbac-homelab`.

The role assignment was applied at the resource-group scope, allowing the managed identity to view resources within the resource group without granting modification permissions.

### 4. Verified the Role Assignment

Reviewed the resource group's **Role assignments** page and confirmed that:

- Principal: `id-rbac-homelab`
- Principal Type: Managed Identity
- Role: `Reader`
- Scope: Resource Group
- Status: Active

### 5. Reviewed the Activity Log

Used the Azure Activity Log to verify that the RBAC role assignment operation was successfully recorded.

## Verification

The RBAC configuration was verified by reviewing the role assignments for the resource group.

The managed identity `id-rbac-homelab` successfully appeared with the `Reader` role assigned at the resource-group scope.

The Azure Activity Log was also reviewed to confirm that the role assignment operation completed successfully.

## Skills Demonstrated

- Azure Resource Group Management
- Azure Role-Based Access Control (RBAC)
- Azure Managed Identities
- Least-Privilege Access
- Access Control (IAM)
- Azure Activity Log Monitoring
- Cloud Security Fundamentals
- Azure Portal Administration
- Technical Documentation
- GitHub Project Documentation

## Lessons Learned

This lab demonstrated the difference between Azure resource permissions and Microsoft Entra directory permissions.

I learned how Azure RBAC can be applied at the resource-group scope and how managed identities can be used as security principals for role assignments.

I also gained hands-on experience with the principle of least privilege by assigning the `Reader` role instead of a higher-privilege role.

Reviewing the Azure Activity Log helped reinforce how administrative changes can be audited and verified after configuration.

## Resume Project Bullet

- Built an Azure RBAC lab by creating a resource group, deploying a user-assigned managed identity, assigning least-privilege `Reader` access through IAM, and validating the role assignment using Azure Activity Logs.

## Screenshots

### Resource Group Created

![Resource Group Created](screenshots/1-creating-resource-group.png)

### Managed Identity Created

![Managed Identity Created](screenshots/2-id-rbac-homelab.png)

### Reader Role Assigned

![Reader Role Assigned](screenshots/3-reader-role-assigned.png)

### RBAC Activity Log

![RBAC Activity Log](screenshots/4-rbac-activity-log.png)
