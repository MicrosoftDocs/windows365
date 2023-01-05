---
# required metadata
title: Windows 365 role-based access
titleSuffix:
description: Learn about role-based access control in Windows 365.
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 01/05/2023 
ms.topic: how-to
ms.service: windows-365
ms.subservice:
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: cohanley
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection: M365-identity-device-management
---

# Role-based access control

Role-based access control (RBAC) helps you manage who has access to your organization's resources and what they can do with those resources. You can assign roles for your Cloud PCs by using the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).

For more information, see [Role-based access control (RBAC) with Microsoft Intune](/mem/intune/fundamentals/role-based-access-control).

## Windows 365 Administrator role

Windows 365 supports the Windows 365 Administrator role available for role assignment through the Microsoft Admin Center and Azure Active Directory (Azure AD). With this role, you can manage Windows 365 Cloud PCs for both Enterprise and Business editions. The Windows 365 Administrator role can grant more scoped permissions than other Azure AD roles like Global Administrator. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference).

## Cloud PC built-in roles

Two built-in roles are available for Cloud PC:

**Cloud PC Administrator**: Manages all aspects of Cloud PCs, like:

- OS image management
- Azure network connection configuration
- Provisioning

**Cloud PC Reader**: Views Cloud PC data available in the Windows 365 node in Microsoft Endpoint Manager, but can’t make changes.

## Custom roles

You can create custom roles for Windows 365 in [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431). For more information, see [Create a custom role]( /mem/intune/fundamentals/create-custom-role).

To create a provisioning policy, an admin needs the following permissions:

- Provisioning Policy Read/Create
- Azure network connection Read
- Supported region Read
- Image Read permissions

<!-- ########################## -->
## Next steps
[Role-based access control (RBAC) with Microsoft Intune](/mem/intune/fundamentals/role-based-access-control).
