---
title: "Data residency for Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/13/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Data residency for Viva Engage"
---

# Data residency for Viva Engage

Viva Engage offers local data residency to help meet data residency requirements. We commit to store message bodies and their file attachments within a specific geographical area, referred to as a *geo*. Viva Engage files are saved in Viva Engage cloud storage. For Microsoft 365 connected groups, some Viva Engage files are stored in SharePoint per your SharePoint data residency policy. Because mobile push notifications send data to a third-party notification service (Apple or Google), they may be outside your geo.

Your Viva Engage Enterprise tenant is automatically created when you create your Microsoft 365 tenant. For Microsoft 365 Education subscribers, your tenant is associated with the US geo. For all other Microsoft 365 subscribers, the country from which you enroll determines your tenant's geo. If you enroll from Europe or Africa, your tenant is associated with the EU geo. If you enroll from Australia, Asia, North America, or South America, your tenant is associated with the US geo.

As of July 2024, all data for reactions (for example, Likes on Viva Engage and Teams Q&A posts) are associated with the tenant’s geo, and are ingested and available for export through eDiscovery. No reactions data are stored outside of the Microsoft 365 boundary.

## Viva Engage features that are unavailable for tenants hosted in the EU geo

Viva Engage Enterprise tenants in the EU geo lack some features that enable full participation between users within your Viva Engage network and users outside your network.

| Viva Engage feature | What this means for the EU geo  |
|:-------|:-------|
| External networks|External networks can't be created in Viva Engage networks (Native Mode or non Native Mode). However, users in the EU geo can join external networks hosted within the US geo.|
|External communities|Viva Engage networks running in non Native Mode can't create external communities. However, on a Viva Engage network running in Native Mode, community admins can add Microsoft 365 users outside of your organization as guests to a community. Learn more about [Microsoft Entra B2B guests in Viva Engage communities](../get-started-with-viva-engage/azure-ad-b2b-guests-viva-engage.md). In addition, users in the EU geo can join external communities on non Native Mode networks hosted in the US geo.|
|External messaging|Users in Viva Engage networks (non Native Mode) can’t add external participants to threads. Users can participate in external messaging threads within networks hosted in the US geo.|
|External collaboration|Viva Engage users in EU geo-hosted networks can't participate in [external messaging threads](../work-with-external-users/external-messaging-faq.md) or add external participants to threads in their Viva Engage Enterprise network. Users on an EU network can participate in a community or external network that’s hosted in the US geo as external guests. This is enabled by the Microsoft B2B   |
|[Posting to Viva Engage by sending an email message](https://support.office.com/article/058d1bc1-3492-47c5-bde2-29ea294acdb6)|This feature is unavailable for legacy Viva Engage networks (non Native Mode) hosted in the EU geo, but is available for all Microsoft 365 connected groups.|

<a name="geodata"></a>

## Determine which geo your tenant is in

Use the following steps to determine the geo in which your tenant resides.

1. Sign in to Viva Engage as a verified admin.

2. Select the **Settings** icon, select **Network Admin** > **Success**.

3. Note the **New Network Checklist** section: 

    - Tenants in the EU geo show **Viva Engage network activated in the EU Geo**.
    - Tenants in the US geo show **Viva Engage network activated in the US Geo**.

## Reprovision your Viva Engage Enterprise network to the EU geo

Customers can have their Viva Engage Enterprise tenant reprovisioned to the Viva Engage EU geo. Contact your Microsoft account team representative for details.

## See also

[Where your Microsoft 365 customer data is stored](/microsoft-365/enterprise/o365-data-locations)