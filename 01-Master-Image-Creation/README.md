# 01 - AVD Master Image Creation

## Overview

This section documents the creation and preparation of a custom master image for an Azure Virtual Desktop (AVD) environment.

The objective was to create a standardized Windows image that could be used to deploy multiple AVD session hosts with consistent applications, configurations, and settings.

## Architecture Flow

Base Windows VM  
↓  
Install Required Applications and Updates  
↓  
Install and Configure FSLogix  
↓  
Clean and Prepare the Operating System  
↓  
Run Sysprep  
↓  
Capture the Master Image  
↓  
Publish the Image to Azure Compute Gallery  
↓  
Deploy AVD Session Hosts from the Custom Image

## Technologies Used

- Microsoft Azure
- Azure Virtual Desktop
- Windows 11 Enterprise Multi-session
- Azure Virtual Machines
- Azure Compute Gallery
- Microsoft Entra ID
- Active Directory Domain Services
- FSLogix
- Azure Files

## Step 1 - Create the Master Image VM

A dedicated Azure virtual machine was created to serve as the master image.

The VM was configured with the required:

- Windows operating system
- Virtual network and subnet
- VM size
- Administrative access
- Required applications
- Windows updates

The master image VM was prepared separately before being used to deploy production-style AVD session hosts.

## Step 2 - Install Required Applications

Required applications and components were installed on the master image VM.

This ensures that all session hosts deployed from the image have a consistent software configuration.

## Step 3 - Install FSLogix

FSLogix was installed on the master image so that session hosts created from the image would have the required FSLogix components.

FSLogix profile configuration was completed separately using the required registry and Azure Files configuration.

## Step 4 - Prepare the Master Image

Before capturing the image, the VM was reviewed and prepared by:

- Installing required Windows updates
- Installing required applications
- Installing FSLogix
- Removing unnecessary temporary files
- Verifying system health
- Preparing the operating system for image capture

## Step 5 - Generalize the VM Using Sysprep

The Windows VM was generalized using Sysprep before image capture.

The following options were used:

- System Cleanup Action: Enter System Out-of-Box Experience (OOBE)
- Generalize: Enabled
- Shutdown Options: Shutdown

After Sysprep completed, the VM was shut down and was not started again before the image capture process.

## Step 6 - Capture the Master Image

The generalized VM was captured as a reusable custom image.

The image was then used with Azure Compute Gallery to support standardized deployment of Azure Virtual Desktop session hosts.

## Result

The custom AVD master image was successfully prepared for session host deployment.

This provides:

- Standardized session host configuration
- Consistent application deployment
- Faster deployment of new session hosts
- Simplified image management
- Improved scalability

## Next Step

The next phase of the project is:

**02 - Azure Compute Gallery and Custom Image Management**
## Implementation Screenshots

### AVD Master Virtual Machine

The following screenshot shows the Azure virtual machine used as the base master image for the Azure Virtual Desktop environment.

![AVD Master Virtual Machine](AVD%20Master.png)
