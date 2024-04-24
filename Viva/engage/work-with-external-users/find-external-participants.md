---
title: "Find external messaging participants in a Viva Engage network"
f1.keywords:
- NOCSH
ms.author: elizapo
author: Starshine89
manager: elizapo
ms.date: 7/11/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 9e8cd010-829a-4d11-8a57-a8f735407604
description: "Viva Engage admins can use data export to find external participants in a network."
---

# Find external messaging participants in a Viva Engage network

*This article applies only to non-Native Mode Viva Engage networks. Additionally, Viva Engage Enterprise networks in the [EU Geo](../manage-security-and-compliance/data-residency.md) don't have external participants.*

When you communicate with outside partners, suppliers, or customers, you want to make sure only authorized personnel have access to the information on your Viva Engage network. Verified admins can use data export to find the names of [external participants](add-external-participants.md) to see which conversations and files in their network are visible to external participants.
  
1. In the Viva Engage admin center, go to **Content and Security** \> **Export data**.

    You'll only see this option if you are a verified admin in the Viva Engage network.

    For more information, see [Export Viva Engage Enterprise data](../eac-as-manage-data.md).

2. To identify **threads in your network that users from other networks participate in**, locate the export folder on your computer, and open the **MessageThreads.Outbound.csv** export file.

    >[!NOTE]
    >The data export reflects the current view of the network. For example, if a user was added, but then removed before the report was created, that user won't appear in the report.
  
    :::image type="content" source="../../media/90261f3d-0629-4fb6-bb42-33ed7eb3e99a.png" alt-text="Screenshot of an example data export file.":::
  
    Column **D** (external_participants) lists the users in other networks that participate in threads in your network, along with their name, email address, and the network ID of the Viva Engage network they belong to.

To remove an external participant, use the list to find the conversation they're included in and remove them from the conversation. See [Remove an external participant from a conversation](add-external-participants.md#RemoveExternal).
  
## Related articles

[Add external participants to your Viva Engage conversations](add-external-participants.md)
  
[External Viva Engage participants FAQ](external-messaging-faq.md)
  
[Disable external messaging in a Viva Engage network](disable-external-messaging.md)
