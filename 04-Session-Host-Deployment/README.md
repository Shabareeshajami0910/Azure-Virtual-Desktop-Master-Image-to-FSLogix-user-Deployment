# 04 - AVD Session Host Deployment from Custom Master Image

## Overview

This section documents the deployment of Azure Virtual Desktop session hosts using the custom master image stored in Azure Compute Gallery.

The objective was to deploy standardized session host virtual machines and register them with the Azure Virtual Desktop host pool.

## Deployment Flow

Custom Master Image  
↓  
Azure Compute Gallery Image Version  
↓  
AVD Host Pool  
↓  
Create Session Host Virtual Machines  
↓  
Configure Networking  
↓  
Join the Required Identity Environment  
↓  
Register Session Hosts with the Host Pool  
↓  
Validate Session Host Availability

## Step 1 - Select the Custom Image

The custom master image stored in Azure Compute Gallery was selected as the source image for the new Azure Virtual Desktop session hosts.

Using a custom image ensures that all deployed session hosts have a consistent:

- Operating system configuration
- Application configuration
- FSLogix installation
- Windows settings
- Required components

## Step 2 - Configure the Session Host Virtual Machines

The required session host settings were configured, including:

- Resource group
- Virtual machine name prefix
- Azure region
- Availability options
- Virtual machine size
- Number of session hosts
- Operating system disk configuration
- Virtual network and subnet

## Step 3 - Configure Network Connectivity

The session hosts were deployed into the required Azure Virtual Network and subnet.

Network connectivity was verified to ensure access to:

- Azure Virtual Desktop services
- Microsoft Entra ID
- Domain services, where required
- Azure Storage
- Azure Files
- Required Microsoft endpoints

## Step 4 - Configure Identity and Domain Connectivity

The session hosts were configured according to the identity architecture used in the environment.

The environment included synchronized identities between on-premises Active Directory Domain Services and Microsoft Entra ID.

The session hosts were configured to support user authentication and access to the required AVD and FSLogix resources.

## Step 5 - Register Session Hosts with the Host Pool

The deployed session hosts were registered with the Azure Virtual Desktop host pool.

After registration, the session hosts were verified in the Azure portal.

The following items were checked:

- Session host registration status
- Availability status
- Agent status
- Assigned users and sessions
- Host pool association

## Step 6 - Validate Session Host Health

The session hosts were validated before user access was provided.

The following checks were performed:

- VM power state
- AVD agent availability
- Network connectivity
- Host pool registration
- User authentication
- Desktop connectivity

## Result

The Azure Virtual Desktop session hosts were successfully deployed from the custom master image and registered with the host pool.

This provided a standardized and repeatable session host deployment process.

## Next Step

The next phase of the project is:

**05 - User Assignment and AVD Desktop Access**
