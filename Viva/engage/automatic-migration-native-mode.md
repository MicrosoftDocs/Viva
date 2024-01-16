---
ms.date: 7/12/2023
title: "Automatic Native Mode migration and network consolidation"
description: "Frequently asked questions about Native Mode for Viva Engage"
ms.reviewer: auhosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Automatic Native Mode migration and network consolidation

Non-native and hybrid Viva Engage networks are being automatically upgraded to Native Mode to allow users, groups, and content to be compatible with and mapped to their counterparts in Microsoft Entra ID and Microsoft 365. Native Mode also provides other benefits, such as the ability to host Live Events in every Viva Engage community and simplify file administration through SharePoint. Most critically, Native Mode supports eDiscovery through the Microsoft Purview compliance portal, allowing your organization to collaborate safely and securely within your Viva Engage network.

 Automatic Native Mode migrations began in December 2022. Support requests for exemptions created after May 26, 2023 won't be approved. Support requests for extensions of existing exemptions won't be approved. Talk to your account team representative if you have further questions.

## Frequently asked questions

### How does automatic migration work?

Unlike manual migration, automatic migration requires little advance preparation. The timeline is:

**10 days before migration starts:** You'll receive a Microsoft 365 Message Center post to notify you that you’ve been selected for automatic migration.

**Day of migration start:** You'll receive a Microsoft 365 Message Center post to notify you that migration has begun.

**During migration:** Migration takes between 1 and 30 days to complete in most cases.

**Once migration is complete:** You'll receive a Microsoft 365 Message Center post to notify you that the migration is complete. You'll have 90 days to perform a post-migration audit or export data not supported in Native Mode.

### I don’t want to be automatically migrated. What can I do?

Native mode is fundamental to the integration of Viva Engage within Microsoft 365 and all networks are being upgraded. Previously, admins had to initiate the migration, but an improved automatic migration is now rolling out.  

If you wish to control the migration, it may still be possible. Start the migration immediately by following the [step-by-step guide](/Viva/engage/native-mode-guide).  

### I received a Microsoft 365 Message Center post that says I’ve been selected for automatic migration. When does it start and end?

Your migration begins 10 days after the date of the Message Center post. You'll receive an additional Message Center post when your migration begins. There is no admin action required to complete the migration. Information about the migration is provided when it completes.

Migration time depends on the volume of files which need to be migrated from legacy Viva Engage file storage to SharePoint storage. It isn't possible to provide an estimate ahead of time due to the number of factors involved.

### I was planning to migrate manually, but the alignment report button is grayed out. How do I export the alignment report?

The alignment report was part of the manual alignment process. When an automatic migration has started, the alignment report is no longer available. This avoids inconsistencies between the report and the state of objects in the network during the automatic migration.

### I want to manually migrate on my own schedule. Is it still possible to receive exemptions?

Exemptions were temporarily available to help customers plan their migrations in the early stages of the rollout of the automated migration process. Now that the automated process is rolling out to all customers and the manual process is being removed from the admin center, it is no longer possible to offer exemptions.  

### What information will be provided after the migration?

All content from your network pre-migration remains available for 90 days. This allows administrators to perform a post-migration audit to ensure completeness of data. Various reports on the migration will be available to administrators, covering deleted unmapped users, deleted files, deleted messages, copied files, and guests.

### What is the impact to end users during the migration?

Community guests need to be reinvited after migration is complete, but most end users aren't impacted during migration. Microsoft Entra B2B replaces the legacy Viva Engage external communities feature when a network is in native mode. See Work with Microsoft Entra B2B guests in Viva Engage communities.

### The migration page says the migration is still in process, but we received a Message Center post stating the migration was complete. What is happening?

The Native Mode migration page will state that the migration is in process until the end of the 90-day data retention period.

### I have more than one network associated with my Microsoft 365 tenant. Will you automatically migrate all of those networks into native mode?

No. Networks will be automatically consolidated soon. You'll receive a Message Center post indicating which network will remain after consolidation. The remaining network will then be migrated to Native Mode. The best way to ensure appropriate network consolidation is to perform it on your own. For more information, see [Consolidate multiple Viva Engage networks](/Viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).
