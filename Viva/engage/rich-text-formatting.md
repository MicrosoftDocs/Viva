---
title: "Rich text formatting for Viva Engage messages"
f1.keywords:
- NOCSH
ms.author: pamgreen
author: ToniSFrench
manager: pamgreen
ms.date: 9/23/2019
audience: Admin
ms.topic: article
ms.service: yammer
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
description: "Users can now format Viva Engage posts using bold, italic, bullets, numbered lists, and links. "
---

# Rich text formatting Viva Engage messages
 
Beginning March 15, 2019, we are rolling out rich text formatting for Viva Engage posts. This includes bold, italic, links, bullets, and numbered lists.

Composing messages with rich text formatting is only available on the web client and Viva Engage app. 

- Composing and viewing formatted messages won't be available immediately on the Viva Engage SharePoint web part or Viva Engage tab in Teams. This functionality will be added later in 2019.

## How do I know if we have rich text available?

If your organization has received this new feature, when you post a new message, here's what the bottom of the message looks like:

![Yammer message with rich text formatting.](../media/with-rich-text.png)

If you don't have rich text, here's what the bottom of the message looks like:

![Yammer message without rich text formatting.](../media/without-rich-text.png)

## Implications for export

When you export formatted messages using [Export Network Data](../manage-security-and-compliance/export-yammer-enterprise-data.md) two columns for the message text are included in messages.csv and messageVersions.csv:
- **body**: includes the unformatted message text 
- **html_body**: includes the message text formatted with HTML
