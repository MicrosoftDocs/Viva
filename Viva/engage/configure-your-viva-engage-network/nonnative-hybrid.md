---
title: "Non-Native Mode and hybrid Viva Engage networks upgrades"
description: Details on non-native and hybrid Viva Engage networks.
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/28/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MET150
- YAE150
---

 # Non-Native Mode and hybrid Viva Engage Network upgrades

 Non-Native Mode and hybrid Viva Engage Networks will be upgraded to [Native Mode](../overview-native-mode.md) to allow users, groups, and content to be compatible with and mapped to their counterparts in Microsoft Entra ID and Microsoft 365. Native Mode also provides other benefits, such as the ability to host live events in every Viva Engage community and simplify file administration through SharePoint. Most critically, Native Mode supports eDiscovery through the Microsoft Purview compliance portal, allowing your organization to collaborate safely and securely within your Viva Engage network. **90% of Viva Engage networks are in Native Mode today, including our top 10 largest networks.**

 ## When does this change happen?

 We began migrating networks December 1, 2022 and continue the upgrades through the third quarter of 2023. The process began with smaller networks. You can initiate the upgrade process on your own by visiting the Microsoft 365 Native Mode page within the Network Admin pages of Viva Engage.

 ## How does this change affect your organization?

 You can no longer access these features:
 -	Network-level guests 
 -	Email blocked lists
 -	Secret groups

 If your organization has active guests, Microsoft Entra B2B guest functionality can be used for guests who reside in the same geographic area as the Viva Engage network. This includes US guests for US networks and EU guests for EU networks. Guests must be reinvited to your network.

If your organization currently uses an email blocked list to manage access to your Viva Engage network, you can continue to manage access from Microsoft Entra ID. Learn more by visiting [Manage Viva Engage licenses in Microsoft 365](../manage-engage-licenses-microsoft-365.md).

These feature equivalents are only available to networks in Native Mode. There's no feature equivalent to secret groups in Microsoft 365. All groups must be public or private.

 As part of the migration process, the Viva Engage administrator account is added to all groups in the network. Files are sometimes renamed.

 ## What do you need to do to prepare?
 **If you would like to self-initiate your migration:**

 There's a [step-by-step guide](../native-mode-guide.md) to Native Mode migration. You can run an alignment report that identifies gaps in your current network alignment with Native Mode. It's critical that you back up your network’s data and communicate the migration to your users before running the Alignment tool mentioned in the guide. This is because some data may be deleted during the process.

 **If you would like Microsoft to initiate your migration:**

 No action is required from you. You can run an alignment report to identify gaps in your current network alignment with Native Mode. **It's strongly recommended that you back up your data and communicate the migration to your users prior to your scheduled migration start date.** If your alignment report reveals any blockers to migration, you can log an exception with support.

 **When you need to postpone or schedule your migration around blackout dates:**

 Contact support to log an exception.
