# 05 - User Assignment and Azure Virtual Desktop Access

## Overview

This section documents the process of assigning users to the Azure Virtual Desktop environment and validating successful access to the published desktop.

The objective was to provide an authorized user with access to the AVD desktop through the Azure Virtual Desktop client.

## User Access Flow

Active Directory User
↓
Microsoft Entra ID Synchronization
↓
AVD Application Group Assignment
↓
Workspace Association
↓
User Authentication
↓
AVD Desktop Connection
↓
Session Host Login

## Step 1 - Verify the User Identity

The user account was verified in Microsoft Entra ID.

The environment used synchronized identities, allowing users created in Active Directory to be synchronized with Microsoft Entra ID.

The following items were verified:

- User account exists
- User synchronization status
- User sign-in availability
- Correct identity is available for AVD assignment

## Step 2 - Assign the User to the Application Group

The required user was assigned to the Azure Virtual Desktop Desktop Application Group.

Navigation:

Azure Portal
→ Azure Virtual Desktop
→ Application Groups
→ Select the Desktop Application Group
→ Assignments
→ Add

The required user was selected and assigned.

## Step 3 - Verify Workspace Association

The Desktop Application Group was associated with the required Azure Virtual Desktop workspace.

The workspace provides the published desktop resource to authorized users.

The following components were verified:

- Host Pool
- Desktop Application Group
- Workspace
- User Assignment

## Step 4 - Sign In to Azure Virtual Desktop

The user signed in to the Azure Virtual Desktop client using the assigned Microsoft Entra ID account.

After successful authentication, the published Session Desktop became available.

## Step 5 - Connect to the Session Host

The user selected the published desktop and successfully connected to the Azure Virtual Desktop session host.

The following items were validated:

- User authentication
- Desktop availability
- Session host connectivity
- Successful Windows session
- User profile creation

## Result

The synchronized user was successfully assigned to the Azure Virtual Desktop environment and was able to access the published desktop.

This confirmed that the AVD user assignment and desktop access configuration were working successfully.

## Next Step

The next phase of the project is:

**06 - Azure Files and FSLogix Profile Configuration**
