---
ms.date: 12/14/2022
title: "Track Viva Engage events in the Microsoft 365 audit log and with the Management Activity API"
description: "You can view Viva Engage events through Microsoft 365 Management API and in the Microsoft 365 Security &amp; compliance portal auditing logs."
ms.reviewer: ethli
ms.author: v-whitfieldd
author: dwhitfield233
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Track Viva Engage events in the Microsoft 365 audit log and with the Management Activity API

To monitor security and compliance-related Viva Engage events for your organization, turn on audit logging and view changes to users, groups, files, admins and network settings. The audit logs are available in the Microsoft 365 Security &amp; compliance portal or by using the Microsoft 365 Management Activity API.
  
You must have the Microsoft 365 global admin role or the Audit Logs role in Exchange online to audit events. You can view Viva Engage events from your home network but not from external networks. You can track the following event categories:
  
- **Users**—includes activate, suspend, and delete a user.

- **Groups**—includes create and delete Microsoft 365 connected Yammer groups. This API doesn't provide data for legacy Yammer groups.

- **Files**—includes create, views, and delete a file.

- **Admins**—includes export data, trigger private content mode, and force all users to sign out.

- **Network settings**—including changing network usage policy and changing data retention policy.

## View the audit sign-in the Microsoft 365 Security &amp; compliance portal

Before you can view the audit log, you need to [turn Microsoft 365 audit log search on or off](https://support.office.com/article/e893b19a-660c-41f2-9074-d3631c95a014). You only have to do this step once. It takes a few hours after you turn it on before you can search the logs.
  
To view the audit log:
  
1. Go to the [Microsoft Purview compliance portal](https://sip.compliance.microsoft.com/homepage) and sign in using your work or school account.

2. In the left pane of the compliance portal, select **Audit**.

3. Follow the instructions to search audit logs as described in [Search the audit sign-in the Microsoft 365 Security and compliance portal](https://support.office.com/article/0d4d0f35-390b-4518-800e-0c7ec95e946c#run).

    :::image type="content" source="../media/track-engage-events-audit-log-inline.png" alt-text="Audit Log Search dialog box." lightbox="../media/track-engage-events-audit-log.png":::
  
## Learn more about the Management API

You can use the Microsoft 365 Management Activity API to download various Viva Engage audit data. Read about how to register your application in Azure AD to get access to these features in [Get started with Microsoft 365 Management APIs](/office/office-365-management-api/get-started-with-office-365-management-apis). For the API reference, see [Microsoft 365 Management Activity API schema](/office/office-365-management-api/office-365-management-activity-api-schema).
  
## Related articles

[Security FAQ](/yammer/manage-security-and-compliance/security-and-compliance#Security)
