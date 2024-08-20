---
ms.date: 08/20/2024
title: "Track Viva Pulse events in the Microsoft 365 audit log"
description: "View Viva Pulse events through Microsoft Purview audit logs."
ms.reviewer: 
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH 
ms.topic: article
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection:  
search.appverid:
---

# Track Viva Pulse events in the Microsoft 365 audit log

To monitor security and compliance-related Viva Pulse events for your organization, turn on audit logging. You can monitor changes to users, groups, files, admins, and network settings. The audit logs are available in the Microsoft 365 Security compliance portal.
  
To audit events, you must have been assigned the Audit Logs role in Microsoft Exchange Online. You can view Viva Pulse events from your home network but not from external networks. You can track the following Viva Pulse events:

- **User created a Pulse survey**—New Viva Pulse feedback request is created.
- **User submitted response to a pulse survey**—User provided feedback for a Viva Pulse feedback request.
- **User extended their pulse survey deadline**—The deadline for the existing Viva Pulse feedback request was extended.
- **User invited additional users to Pulse survey**—More users were invited to an existing Viva Pulse feedback request.
- **User canceled a Pulse survey**—User canceled a Pulse survey.
- **User shared a pulse report**—Viva Pulse feedback result was shared with users.
- **User created a Pulse draft**—User created a Pulse draft.
- **User deleted a Pulse draft**—User deleted a Pulse draft.
- **Admin deleted an user's data**—Admin deleted a user's data.
- **User starts a new Pulse report conversation**—User responds to a Pulse open text response to start a new conversation in a Pules report.
- **User responds to a Pulse report conversation**—User responds to an existing conversation in a Pulse report.
- **User deletes a Pulse report conversation message**—Admin or User deletes a message that is part of a conversation in a Pulse report.
- **Admin updated tenant's settings**—Admin updated an organization setting for Viva Pulse.


## View the audit sign-in the Microsoft 365 Security &amp; compliance portal

Before you can view the audit log, you need to turn on [Microsoft 365 audit log search](https://support.office.com/article/e893b19a-660c-41f2-9074-d3631c95a014). You only have to do this step once. It can take a few hours after you turn it on before you can search the logs.
  
To view the audit log:
  
1. Go to the [Microsoft Purview compliance portal](https://compliance.microsoft.com/homepage) and sign in using your work or school account.

2. In the left pane of the compliance portal, select **Audit**.

3. Follow the instructions to search audit logs as described in [Search the audit sign-in the Microsoft 365 Security and compliance portal](https://support.office.com/article/0d4d0f35-390b-4518-800e-0c7ec95e946c#run).


## Related articles

[Viva Pulse Activities](https://go.microsoft.com/fwlink/?linkid=2283466)
