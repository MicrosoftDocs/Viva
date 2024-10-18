---
title: "Rich text formatting for Viva Engage posts"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 9/11/2024
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
 
Viva Engage offers rich text formatting for your posts. Formatting options include bold, italic, links, bullets, and numbered lists. 

You can compose messages with rich text formatting on the Viva Engage mobile app, desktop app, and web client. Additionally, Engage feeds in SharePoint (through the Conversations web part) also offer rich text formatting.

When you post a new message, you'll find a menu at the bottom of your message with these formatting options.

## Implications for export

When you export formatted messages using [Export Network Data](../manage-security-and-compliance/export-viva-engage-enterprise-data.md) two columns for the message text are included in messages.csv and messageVersions.csv:

- **body**: includes the unformatted message text 
- **html_body**: includes the message text formatted with HTML
