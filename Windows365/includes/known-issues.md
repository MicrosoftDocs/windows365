---
title: include file
description: include file
author: ErikjeMS  
ms.service: cloudpc
ms.topic: include
ms.date: 02/08/2022
ms.author: erikje
ms.custom: include file
---

## Missing start menu and taskbar when using iPad and the Remote Desktop app to access a Cloud PC

When non-local admin users sign in to a Cloud PC by uinsg an iPad and the Microsoft Remote Desktop app, the start menu and task bar might be missing from the Windows 11 user interface.

**Troubleshooting steps**: Make sure that you have the latest version of Remote Desktop Client as found [here](/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients).
In addition, you can also sign in to the Cloud PC by using [windows365.microsoft.com](https://windows365.microsoft.com).

## Restore and automatic rolling credentials

Many devices registered with Active Directory might have a machine account password that is automatically updated. By default, these passwords are updated every 30 days. This automation applies to hybrid joined PCs but not Azure Active Directory Native PCs.

The machine account password is maintained on the Cloud PC. If the Cloud PC is restored to a point that has a previous password stored, the Cloud PC won't be able to sign onto the domain.

For more information, see [Machine Account Password Process](https://techcommunity.microsoft.com/t5/ask-the-directory-services-team/machine-account-password-process/ba-p/396026).