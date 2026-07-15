# 03 - Azure Virtual Desktop Host Pool Deployment

## Overview

This section documents the creation and configuration of an Azure Virtual Desktop (AVD) host pool.

The host pool provides the logical grouping and management layer for the Azure Virtual Desktop session hosts deployed from the custom master image.

## Deployment Flow

Azure Virtual Desktop  
↓  
Create Host Pool  
↓  
Configure Host Pool Type  
↓  
Configure Load Balancing  
↓  
Create Application Group  
↓  
Associate Application Group with Workspace  
↓  
Prepare for Session Host Deployment

## Step 1 - Create the Host Pool

A new Azure Virtual Desktop host pool was created in the Azure portal.

The host pool acts as a collection of Azure virtual machines that provide desktops and applications to assigned users.

## Step 2 - Configure Host Pool Type

The host pool was configured according to the lab requirements.

Azure Virtual Desktop supports:

### Pooled Host Pool

Multiple users can connect to available session hosts in the host pool.

This model is suitable for:

- Shared desktop environments
- Multi-session workloads
- Cost optimization
- Dynamic user distribution

### Personal Host Pool

A dedicated session host is assigned to an individual user.

This model is suitable for:

- Dedicated user desktops
- Persistent workloads
- User-specific VM assignments

For this project, the host pool configuration was selected based on the required AVD deployment architecture.

## Step 3 - Configure Load Balancing

For a pooled host pool, the load-balancing method determines how user sessions are distributed across available session hosts.

The available methods include:

- Breadth-first
- Depth-first

Breadth-first distributes users across multiple available session hosts.

Depth-first fills one session host before directing users to another available session host.

## Step 4 - Create the Desktop Application Group

A Desktop Application Group was created for the host pool.

The Desktop Application Group allows authorized users to access the full Azure Virtual Desktop desktop experience.

## Step 5 - Create or Associate a Workspace

The Application Group was associated with an Azure Virtual Desktop workspace.

The workspace provides users with access to their assigned desktop resources through supported Azure Virtual Desktop clients.

## Step 6 - Validate the Host Pool

The host pool configuration was verified before deploying the session hosts.

The following components were validated:

- Host pool configuration
- Host pool type
- Load-balancing configuration
- Desktop Application Group
- Workspace association

## Result

The Azure Virtual Desktop host pool was successfully created and prepared for session host deployment.
