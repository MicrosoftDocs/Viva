---
title: "Data residency for Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-cdemaagd
author: cedemaagd
manager: dmillerdyson
ms.date: 6/28/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Data residency for Viva Engage"
---

# Data residency for Viva Engage
Viva Engage offers local data residency to help meet data residency requirements. We commit to store message bodies and files attached to messages at rest within a specific geographical area (Geo). Viva Engage files are saved either in Viva Engage cloud storage, or for Microsoft 365 connected groups, some Viva Engage files are stored in SharePoint. Viva Engage files saved in SharePoint will be stored in SharePoint Online per your SharePoint Online data residency policy. Mobile push notifications require sending data to a third-party notification service (Apple or Google), which might be outside your Geo.

Your Viva Engage Enterprise tenant is automatically created when you create your Office 365 tenant. For Office 365 Education subscribers, your tenant is associated with the US Geo. For all other Microsoft 365 or Office 365 subscribers, the country you enroll from determines the Geo your tenant is associated with. When you enroll from Europe or Africa your tenant is associated with the EU Geo and when you enroll from Australia, Asia, North America, or South America your tenant is associated with the US Geo.

### Features not available for Viva Engage tenants in the EU Geo

The following Viva Engage features are not available for Viva Engage tenants in the EU Geo:

- All external collaboration features:

    - Only users in your Office 365 tenant can participate in your Viva Engage Enterprise tenant.

    - External guests can't participate in your Viva Engage Enterprise tenant.

    - Your users can't participate in other Viva Engage networks, including external tenants.

    - Your users can't be participants in [external messaging threads, or add external participants to threads](../work-with-external-users/external-messaging-faq.md) in your Viva Engage Enterprise network.

    - External groups can't be created in your Viva Engage Enterprise tenant, and your users can't participate in external groups belonging to other tenants.

- [Posting to Viva Engage by sending an email message](https://support.office.com/article/058d1bc1-3492-47c5-bde2-29ea294acdb6) is only available for Microsoft 365 connected groups.


<a name="geodata"></a>

##  Determine which Geo your tenant is in

1. Log in to Viva Engage as a Verified Admin.

2. Click the **Settings** icon, click **Network Admin**, and then click **Success**. 

3. In the **New Network Checklist** section: 

    - If your tenant is in the EU, you'll see **Viva Engage network activated in the EU Geo**.

    - If your tenant is in the US, you'll see **Viva Engage network activated in the US Geo**.

##  Reprovision your Viva Engage Enterprise network to EU Geo
Customers can have their Viva Engage Enterprise tenant reprovisioned to the Viva Engage EU Geo. Please talk to your Microsoft account team representative for details.

## See also

[Where is your Microsoft 365 or Office 365 data located](/microsoft-365/enterprise/o365-data-locations)

[How do I tell where my Viva Engage files are being stored?](https://support.office.com/article/how-do-i-tell-where-my-yammer-files-are-being-stored-fadfdefa-e00d-40b6-94cb-a9ddb171a443)
