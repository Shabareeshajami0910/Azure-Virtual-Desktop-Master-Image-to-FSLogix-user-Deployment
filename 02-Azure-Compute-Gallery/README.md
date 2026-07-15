# 02 - Azure Compute Gallery and Custom Image Management

## Overview

This section documents the process of storing and managing the generalized Azure Virtual Desktop master image using Azure Compute Gallery.

Azure Compute Gallery provides centralized image management and allows a standardized custom image to be used for deploying multiple Azure Virtual Desktop session hosts.

## Architecture Flow

Generalized Master Image VM  
↓  
Azure Compute Gallery  
↓  
Image Definition  
↓  
Image Version  
↓  
AVD Session Host Deployment

## Step 1 - Create Azure Compute Gallery

An Azure Compute Gallery was created to centrally manage the custom Azure Virtual Desktop image.

The gallery provides:

- Centralized image management
- Image versioning
- Reusable custom images
- Support for standardized VM deployment
- Improved management of AVD session host images

## Step 2 - Create an Image Definition

An image definition was created inside the Azure Compute Gallery.

The image definition contains information about the operating system and image configuration.

The following settings were defined:

- Operating system type
- Operating system state
- VM generation
- Publisher
- Offer
- SKU

The operating system state was configured as **Generalized** because Sysprep was performed on the master image.

## Step 3 - Create an Image Version

After the master VM was generalized, an image version was created.

The generalized master image was used as the source for the image version.

Image versioning allows future updates to the master image while maintaining previous versions when required.

Example versioning strategy:

- 1.0.0 - Initial master image
- 1.0.1 - Application updates
- 1.1.0 - Major configuration changes

## Step 4 - Validate the Image

After image creation, the image version was verified in Azure Compute Gallery.

The image was then available as a source for deploying new Azure Virtual Desktop session hosts.

## Result

The custom AVD master image was successfully stored and managed using Azure Compute Gallery.

This enables:

- Consistent session host deployments
- Centralized image management
- Image version control
- Faster deployment of additional session hosts
- Easier image lifecycle management

## Next Step

The next phase of the project is:

**03 - Azure Virtual Desktop Host Pool Deployment**
