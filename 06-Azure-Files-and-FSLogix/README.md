# 06 - Azure Files and FSLogix Profile Configuration

## Overview

This section documents the implementation of FSLogix Profile Containers for the Azure Virtual Desktop environment.

The objective was to store user profiles centrally in an Azure Files share instead of keeping user profiles only on individual AVD session hosts.

The final solution used:

- Azure Files
- Microsoft Entra Kerberos authentication
- Microsoft Entra synchronized user identity
- FSLogix Profile Containers
- Azure Virtual Desktop Session Host

---

## Architecture Flow

User signs in to Azure Virtual Desktop

↓

User connects to the AVD Session Host

↓

Microsoft Entra Kerberos authentication is used

↓

Session Host accesses the Azure Files share

↓

FSLogix creates or attaches the user's VHD profile container

↓

User profile is loaded inside the AVD session

---

## Step 1 - Create the Storage Account

An Azure Storage Account was created to store the FSLogix user profile containers.

The storage account was configured to support Azure Files.

The storage account endpoint used in this lab was:

`masterfslogix.file.core.windows.net`

> Note: Storage account names and resource names shown in this repository are lab examples.

---

## Step 2 - Create the Azure File Share

A file share named `profiles` was created inside the storage account.

The UNC path used by FSLogix was:

`\\masterfslogix.file.core.windows.net\profiles`

This file share acts as the central location for storing FSLogix user profile containers.

---

## Step 3 - Configure Microsoft Entra Kerberos

Microsoft Entra Kerberos authentication was configured for the Azure Storage Account.

This allows Microsoft Entra identities to authenticate to the Azure Files share using Kerberos.

The configuration was validated from the AVD session host.

---

## Step 4 - Validate Cloud Kerberos

The following command was used to check the Cloud Kerberos configuration:

```cmd
klist cloud_debug
