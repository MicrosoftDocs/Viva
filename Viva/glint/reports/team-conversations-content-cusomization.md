---
title: Customize Viva Glint Team Conversation email content
description: Customize Microsoft Viva Glint email content for Team Conversation start messages and reminders in the Communications section of Program Setup.
ms.author: aweixelman
author: AliciaWeixelman
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: start email, reminder, team conversations
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/26/2024
---

# Customize Viva Glint Team Conversation email content

Customize Microsoft Viva Glint email content for Team Conversation start messages and reminders in the Communications section of Program Setup. Optionally, set up a custom email sending domain and a company logo for emails. To understand how to enable/disable emails, and for more information about Team Conversations setup, see [Admin setup for Viva Glint Team Conversations](team-conversations-administrator-setup.md).

> [!NOTE]
> Email content customization is currently only available to some Viva Glint customers. All Viva Glint customers will have email content edit abilities with a new email provider soon.

## Custom sending domains and themes/logos (optional)

In the [Microsoft Admin Center (MAC)](https://go.microsoft.com/fwlink/?linkid=2264234), your M365 admin can optionally configure a custom sending domain for your organization and customize your organization's theme to include your logo in survey communications:

- [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products)
- [Customize the Microsoft 365 theme for your organization](/microsoft-365/admin/setup/customize-your-organization-theme)

Both items are **optional steps** that your organization can take to further customize the survey communication experience for your survey participants.

> [!NOTE]
> - Custom sending domains configured in MAC can impact other M365 products. See [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products) for a full list.
> - Viva Glint teams have access to limited email delivery metrics. Using a custom sender domain gives your organization direct access to your email delivery data.

## Email sections

To edit email content, go to the Communications section of your desired survey program, select the pencil icon to edit a given Team Conversations email, and in the edit pane that appears, select the pencil icon to edit content.

Viva Glint Conversation Start, reminders, and summary notifications contain multiple editable sections:

:::image type="content" source="../../media/glint/setup/glint-tc-sections.png" alt-text="Screenshot of editable Team Conversation start email sections in Viva Glint.":::

Add your customizations to each section and select **Save Changes** in the top right to save all of your edits.

> [!CAUTION]
> Hyperlinks and HTML aren't supported content in Viva Glint customized emails. These items can cause email delivery/blocking issues.

### Email macros

Macros in Viva Glint emails allow your organization to add placeholders that pull in information from your employee data and from Viva Glint. Include Departments, Manager Names, or additional Team Conversation information in email text to further customize for managers. To add a macro, select the plus sign icon email sections where it exists and choose a macro from the dropdown menu.

:::image type="content" source="../../media/glint/setup/glint-tc-macros.png" alt-text="Screenshot of macros available to add to Team Conversation email text.":::

## Manage translations

Any edits made to email text in English need to be made to all other survey languages. Use either of the methods below to manage your Team Conversation email translations.

### Use the language dropdown

In the email edit pane, after customizing English content, use the **Language** dropdown menu to select other survey languages and add translations to each section. Select **Save Changes** in the top right to save all of your edits.

:::image type="content" source="../../media/glint/setup/glint-email-language-dropdown.png" alt-text="Screenshot of the Language dropdown in the email edit pane.":::

### Use the program content import

Use this [translation guidance](/setup/language-translations) to import updated translations for emails after modifying English text.
