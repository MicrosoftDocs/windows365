---
# required metadata
title: Compare Windows 365 Business and Enterprise
titleSuffix:
description: What are the differences between Windows 365 Business and Enterprise?
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 02/08/2022
ms.topic: overview
ms.service: cloudpc
ms.subservice:
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: naramkri
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection: M365-identity-device-management
---

# Compare Windows 365 Business and Enterprise

Windows 365 is available in two editions: [Windows 365 Business](./business/index.yml) and [Windows 365 Enterprise](./enterprise/index.yml).

## General comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Domain Join | Azure AD Join without Azure Virtual Network (VNet) support. | Azure AD Join without VNet support.<br>Azure AD Join with VNet support.<br>Hybrid Azure AD with VNet support.<br>For other domain support, see [In development for Windows 365 Enterprise](./enterprise/in-development.md). |

## Purchasing and licensing comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Purchase channels | Web direct, self-service, Cloud Solution Provider (CSP). | Web direct, Enterprise Agreements (EA), CSP. |
| License assignment | Microsoft 365 Admin Center or the Azure AD portal. | Microsoft 365 Admin Center or the Azure AD portal. |
| Licensing requirements | No licensing pre-requirements to buy and deploy Windows 365 Business. Other features (like device management) can be used if users are licensed for Microsoft Endpoint Management.| Each user must be licensed for Windows 10 or 11 Enterprise (when available), Microsoft Endpoint Manager, and Azure AD P1. |
| Networking costs | Outbound data/month is based on the RAM of the Cloud PC:<br>- 2-GB RAM = 12-GB outbound data<br>- 4 or 8-GB RAM = 20-GB outbound data<br>- 16-GB RAM = 40-GB outbound data<br>- 32-GB RAM = 70-GB outbound data<br>Data bandwidth may be restricted when these levels are exceeded. | When providing a network, Networking goes through the customer's Azure VNet and isn't included in the license. [Azure bandwidth pricing](https://azure.microsoft.com/pricing/details/bandwidth/) applies for these network usage costs. <br>If using a Microsoft-hosted network, the same charges (as described in Windows 365 Business networking charges) apply.|
| Seat limits | Capped to 300 seats per tenant. [Commercial Licensing Terms](https://www.microsoft.com/licensing/terms/productoffering/Windows365/MOSA) | No seat cap per tenant. [Commercial Licensing Terms](https://www.microsoft.com/licensing/terms/productoffering/Windows365/MOSA) |

## Administrative comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Provisioning | Provisioning is simplified and uses default configurations.<br>Cloud PCs are automatically provisioned with a standard image after a Cloud PC license is assigned. | Provisioning is configurable and customizable to the needs of the organization.<br>Admins select the network, configure user permissions (local admin or not), and assign the policy to an Azure AD group.<br>Cloud PCs are then provisioned by using standard gallery images or custom images (admin choice). |
| Policy management | Not Supported. | Group Policy Objects (GPO) and Intune MDM are supported. |
| Application deployment | Supported only if you have Intune license. | Supported. |
| Windows updates | Default Windows Update for Business settings are configured for users. With an Intune license, these settings can be edited. | Can be managed by using Microsoft Endpoint Manager. |
| Device management | Device management is limited to assigning and unassigning of Cloud PC licenses in the Microsoft Admin Center. Some device management is possible in Microsoft Endpoint Manager if you have an Intune license but Cloud PCs won't be visible in the Windows 365 blade. | Microsoft Endpoint Manager admin center options, including image management, link and access on-premises resources, granular targeting of policies, resizing Cloud PCs, other user experience settings, and all the policy-based management options available to physical devices. |
| Monitoring | Not supported. | Endpoint Analytics reporting and monitoring, service health, and operational health alerts. |
| Troubleshooting | Not supported | Microsoft Endpoint Manager troubleshooting including the Troubleshooting blade, device management actions, and reprovisioning of Cloud PCs to their initial state. |
| Partner/programmatic access | Not supported | Partners can manage Cloud PCs through Microsoft 365 Lighthouse or restful web APIs (Graph) to support Managed Service Provider tooling for up to 300 seats.  |

## End user comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Management | Users can [restart, reset, rename, and troubleshoot](./business/get-users-started.md#user-actions) their Cloud PCs on the Windows 365 homepage. | Users can [restart, rename, and troubleshoot](./enterprise/end-user-access-cloud-pc.md) their Cloud PCs on the Windows 365 homepage. |
| Role | By default, each user is assigned the Local Administrator role on their Cloud PC. This supports the native installation of Win32 apps. This can't be changed by the Global Administrator. | By default, each user is assigned a standard user role on their Cloud PC. This can be changed by the admin in the Microsoft Endpoint Manager admin center.|
| Access | Users can access their Cloud PC at windows365.microsoft.com or by using Microsoft Remote Desktop. | Users can access their Cloud PC at windows365.microsoft.com or by using Microsoft Remote Desktop. |
| Platform | Any platform that supports Microsoft Remote Desktop clients. [Learn more.](/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients)  | Any platform that supports Microsoft Remote Desktop clients. [Learn more.](/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients)  |

## Security comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Conditional Access | Conditional Access policies can be deployed only by using Azure AD with an Azure AD P1 license. | Conditional Access policies can be deployed by using the Microsoft Endpoint Manager admin center or Azure AD. |
| [Per-user multi-factor authentication (MFA)](/azure/active-directory/authentication/howto-mfa-userstates) | Only MFA using [Azure AD Conditional Access](/azure/active-directory/authentication/tutorial-enable-azure-mfa) is supported. Legacy per-user MFA isn't supported. | Legacy per-user MFA is supported for user connections to Hybrid Azure AD joined Cloud PCs.  It's not supported for user connections to Azure AD joined Cloud PCs. |
| Security baselines | Not supported. | Dedicated Security Baselines can be edited and deployed by using Microsoft Endpoint Manager. |
| Microsoft Defender for Endpoint | Supported if the customer separately has the requisite E5 license. | Integration with Defender for Endpoint. If the customer has an E5 license, all Cloud PCs will respond to Defender for Endpoint policies and show up in MDE dashboards. |

## Support comparisons

| Capability | Windows 365 Business | Windows 365 Enterprise |
| --- | --- | --- |
| Support channels | Support tickets can be filed through the Microsoft 365 Admin Center. | Support tickets can be filed through Microsoft Endpoint Manager (recommended) and the Microsoft 365 Admin Center. |

<!-- ########################## -->
## Next steps

For more information about Windows 365 Enterprise, see [What is Windows 365 Enterprise?](./enterprise/overview.md).

For more information about Windows 365 Business, see [Getting started with Windows 365 Business and Cloud PCs](./business/get-started-windows-365-business.md).
