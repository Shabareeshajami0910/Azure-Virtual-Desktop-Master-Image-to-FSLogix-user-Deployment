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
