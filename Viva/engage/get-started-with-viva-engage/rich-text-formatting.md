---
title: "Rich text formatting for Viva Engage posts"
f1.keywords:
- NOCSH
ms.author: v-bvrana
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
description: "Users can now format Viva Engage posts using bold, italic, bullets, numbered lists, and links. "
---

# Rich text formatting for Viva Engage posts
 
Beginning March 15, 2019, we offer rich text formatting for Viva Engage posts. Formatting options include bold, italic, links, bullets, and numbered lists.

Composing messages with rich text formatting is only available on the web client and Viva Engage desktop.

- Mobile Viva Engage apps display formatted messages, but users can't edit those messages or format new messages from the mobile device.

- Composing and viewing formatted messages aren't available immediately on the Viva Engage SharePoint web part or Viva Engage tab in Teams. This functionality will be added later in 2019.

## How do I know if we have rich text available?

If your organization has received this feature, when you post a new message, you'll find a menu at the bottom of your message with formatting options. If you don't have this feature, the area at the bottom of the message is blank.

## Implications for export

When you export formatted messages using [Export Network Data](../manage-security-and-compliance/export-viva-engage-enterprise-data.md) two columns for the message text are included in messages.csv and messageVersions.csv:
- **body**: includes the unformatted message text 
- **html_body**: includes the message text formatted with HTML
