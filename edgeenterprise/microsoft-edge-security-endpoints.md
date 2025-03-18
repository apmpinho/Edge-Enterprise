---
title: "Allowlist for Microsoft Edge endpoints"
ms.author: leahtu
author: dan-wesley
manager: archandr
ms.date: 12/18/2024
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Allow list for Microsoft Edge endpoints"
---

# Allow list for Microsoft Edge endpoints

Microsoft Edge requires connectivity to the Internet to support its features. This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.

> [!NOTE]
> Applies to Microsoft Edge version 77 or later.

## Domain URLs to allow

Allow the following domain URLs for Microsoft Edge.

### Update Service

The service that Microsoft Edge uses to check for new updates.

- `https://msedge.api.cdp.microsoft.com`

### Experimentation and Configuration service

- `https://config.edge.skype.com`

### Download locations for Microsoft Edge

Locations Microsoft Edge can be downloaded from during an initial install or when an update is available. The download location determined by the Update Service.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > To simplify the allow list for download locations a wild card can be used: `*.dl.delivery.mp.microsoft.com`

### Download locations for Microsoft Edge Extensions

Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available. The download location determined by the Update Service.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > To simplify the allowlist for download locations a wild card can be used: `*.dl.delivery.mp.microsoft.com`

### Tab groups

The service that supports AI-assisted tab group features. Auto-named tab groups automatically name tab groups upon creation and organize tabs groups tabs by relevance and assigns them a name and a color.

- `https://edge.microsoft.com/taggrouptitlegeneration/api/TitleGeneration/gen/`
- `https://edge.microsoft.com/taggrouptitlegeneration/api/AutoGrouping/groupingacstreaming`

### Optionally for Download Delivery Optimization

For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](/windows/deployment/update/waas-delivery-optimization).

- Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)
- Client to Client communication: TCP port 7680 should be open for inbound traffic

### Sign In

These endpoints are required for profile sign in to work correctly, both for Microsoft and Entra accounts.

- `https://login.live.com`
- `https://login.microsoftonline.com`
- `https://login.microsoft.com`
- `https://login.windows.net`
- `https://odc.officeapps.live.com`
- `https://graph.microsoft.com`
- `https://substrate.office.com`
- `https://privacy.microsoft.com`
- `https://cdn.odc.officeapps.live.com`
- `https://logincdn.msauth.net`

### Sync

These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.

- Microsoft Edge sync service endpoints:

  - `https://edge.microsoft.com`

- Azure Information Protection endpoints:

  - `https://api.aadrm.com` (for most tenants)
  - `https://api.aadrm.de` (for tenants in Germany)
  - `https://api.aadrm.cn` (for tenants in China)

- Microsoft Edge cloud messaging service endpoints:
 
   - `https://*.cloudmessaging.edge.microsoft.com/` 
   - `wss://*.cloudmessaging.edge.microsoft.com/`
   

### Cloud Site List Management

The service that Microsoft Edge uses to download the cloud-hosted site list for Internet Explorer (IE) mode. For more information, see [Cloud Site List Management](https://aka.ms/CloudSiteList)

- `https://edge.microsoft.com/`

### Microsoft Edge management service

The service that Microsoft Edge uses to download the configuration profiles. For more information, see [Microsoft Edge management service](/deployedge/microsoft-edge-management-service).

- `https://edge.microsoft.com/`
- `https://clients.config.office.net`

## Microsoft Defender SmartScreen services

[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) helps protect users from malicious sites and downloads.

- `https://*.smartscreen.microsoft.com/`
- `https://*.smartscreen-prod.microsoft.com`
- `https://*.urs.microsoft.com/`

## Copilot and Sidebar

The service that supports Copilot, and other apps, in the Microsoft Edge sidebar.

- `http://edgeservices.bing.com/`
- `https://edgeservices.bing.com/`

> [!NOTE]
> Other endpoints that Copilot requires to function can be found in the [Copilot network requirements](/copilot/manage#network-requirements).

## Microsoft Rewards

The service that supports Microsoft Rewards.  

- `https://prod.rewardsplatform.microsoft.com/`

## Web Content Filtering

The service that supports Web Content Filtering. For more information, see [Configure Web Content Filtering on Microsoft Edge](/deployedge/microsoft-edge-web-content-filtering).

- `https://edge.microsoft.com/webcontentfiltering/api/categories`
- `https://edge.microsoft.com/webcontentfiltering/api/guestmode-categories`
- `https://edge.microsoft.com/webcontentfiltering/settings/v1`

## Feedback and Diagnostics

The service that supports feedback and diagnostics for desktop and mobile users.

- `https://api.msa.diagnostics.office.com`
- `https://api.diagnostics.office.com`

## Other browser support services

Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates. Provide downloadable spellcheck dictionaries and ad-blocking blocklists. Provide services to support browser features such as collections, autofill, and extension store.

#### HTTP

- `http://edge.microsoft.com/`
- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://edge.microsoft.com/`
- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge documentation landing page](./index.yml)
- [Manage connection endpoints for Windows 10 Enterprise, version 1903](/windows/privacy/manage-windows-1903-endpoints)
