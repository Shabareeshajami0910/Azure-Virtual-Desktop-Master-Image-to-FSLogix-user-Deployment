[14:35, 15/07/2026] Shabareesha: ## Implementation Screenshots

### AVD Master Virtual Machine

The following screenshot shows the Azure virtual machine used as the base master image for the Azure Virtual Desktop environment.

![AVD Master Virtual Machine](AVD%20Master.png)
[14:39, 15/07/2026] Shabareesha: ### Applications Installed on the Master Image

The following screenshot shows the applications installed and configured on the AVD master image before generalization.

![Master Image Installed Applications](EXACT-FILENAME-HERE.png)
[14:42, 15/07/2026] Shabareesha: # Azure Virtual Desktop: Master Image to FSLogix User Deployment

## Project Overview

This project demonstrates an end-to-end implementation of an Azure Virtual Desktop (AVD) environment, starting with the creation of a custom master image and continuing through Azure Compute Gallery, AVD host pool deployment, session host deployment, user assignment, Microsoft Entra authentication, Azure Files, and FSLogix Profile Containers.

The objective of this project was to build a standardized and scalable Azure Virtual Desktop environment while gaining hands-on experience with image management, session host deployment, user access, authentication, and profile management.

---

## Project Architecture

The implementation follows this high-level flow:

```text
Custom Windows Master VM
        ↓
Install Applications and Configure the OS
        ↓
Sysprep and Generalize the Master VM
        ↓
Azure Compute Gallery
        ↓
Custom Image Version
        ↓
Azure Virtual Desktop Host Pool
        ↓
Session Host Deployment
        ↓
Desktop Application Group
        ↓
User Assignment
        ↓
Microsoft Entra Authentication
        ↓
Azure Files
        ↓
FSLogix Profile Container
        ↓
Successful AVD User Session
