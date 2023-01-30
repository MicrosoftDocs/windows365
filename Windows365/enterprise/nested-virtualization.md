---
# required metadata
title: Set up virtualization-based workloads on your Windows 365 Cloud PC.
titleSuffix:
description: Learn how to set up nested virtualization on your Windows 365 Cloud PC.
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 07/07/2022
ms.topic: how-to
ms.service: windows-365
ms.subservice:
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: chbrinkh
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection: M365-identity-device-management
---

# Set up virtualization-based workloads support

Virtualization-based workloads let customers use the following systems on their Windows 365 Enterprise Cloud PCs:

- Windows Subsystem for Linux (WSL)
- Windows Subsystem for Android
- Sandbox
- Hyper-V  

## Requirements

To use virtualization-based workloads, the Cloud PC must meet these requirements:

- 8vCPU/32 Cloud PC (Downsizing to 4vCPU or 2vCPU Cloud PCs will disable nested virtualization)
- Be in one of these regions (other regions aren't currently supported):
  - US East
  - US East 2
  - US West 3
  - US South central
  - Australia East
  - Europe North
  - Europe West
  - UK South
  - Canada Central
  - India Central
  - Japan East
  - France Central

## Set up virtualization-based workloads

1. If the Cloud PC was provisioned before April 5, 2022, you must [reprovision](reprovision-cloud-pc.md) the Cloud PC.
2. To set up a specific virtualization-based workloads system, see the following articles:
    - [Set up a WSL development environment](/windows/wsl/setup/environment).
    - [Windows Subsystem for Android™️](/windows/android/wsa/).
    - [Install Hyper-V on Windows 10](/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v).


<!-- ########################## -->
## Next steps

For more information about virtualization-based workloads, see [Run Hyper-V in a Virtual Machine with Nested Virtualization](/virtualization/hyper-v-on-windows/user-guide/nested-virtualization).
