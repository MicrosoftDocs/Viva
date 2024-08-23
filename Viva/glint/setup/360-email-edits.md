---
title: Customize Viva Glint 360 email content 
description: The  Microsoft 365 admin can configure a custom email domain for your organization
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: viva glint 360s, 360 emails, custom content, custom email, customize 360 email
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 8/23/2024
---

# Customize Viva Glint 360 email content 

## Custom sending domains and branding (optional)

In the [Microsoft 365 Admin Center (MAC)](https://go.microsoft.com/fwlink/?linkid=2264234), your Microsoft 365 admin can optionally configure a custom email domain for your organization. In the [Microsoft Entra admin center](https://entra.microsoft.com/#home), customize your organization's branding to include your logo in 360 survey communications:

- [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products)
- [Customize company branding](/microsoft-365/admin/setup/customize-sign-in-page)

Both items are **optional steps** that your organization can take to further customize the 360 communication experience for your survey participants.

> [!NOTE]
> - Custom sending domains configured in MAC can impact other M365 products. See [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products) for a full list.
> - Viva Glint teams have access to limited email delivery metrics. Using a custom sender domain gives your organization direct access to your email delivery data.

## Email customizations

To edit Viva Glint 360 email content: 

1. Go to the **Schedule & Communication** section of your desired 360 cycle. 
2. In the **360 Communication Triggers & Notifications** section, select the pencil icon on the far right of a 360 email to edit and preview content. Editable emails include:
   - Welcome and Feedback Provider Selection
   - Give Feedback Invitation
   - Response Rate Email
   - Report Ready to Subject
   - Report Ready to Subject's Coach
   - Report Ready to Additional Person (off by default)
   - Report Ready to Subject's Manager
3. In the edit pane that appears, select the pencil icon to edit content.
4. Viva Glint 360 emails and reminders contain multiple editable sections:

   :::image type="content" source="../../media/glint/setup/360-welcome-email-edit.png" alt-text="Screenshot      of editable 360 email sections in the Welcome and Feedback Provider Selection email.":::

5. Add your customizations to each section and select **Save Changes** in the top right to save all of your edits.
6. Preview edits by selecting the eye icon in the email edit pane to view emails in the platform.
7. Repeat these steps for all 360 emails that need customizations for your organization.


> [!CAUTION]
> Hyperlinks and HTML aren't supported content in Viva Glint customized emails. These items can cause email delivery/blocking issues.

### Email macros

Macros in Viva Glint 360 emails allow your organization to add Viva Glint placeholders that pull in information based on users' names in your employee data. For example, include Subject Due Date, Days to Complete Feedback, or Feedback Cycle Name in email text to further customize for 360 survey participants. To add a macro, select the plus sign icon in email sections where it exists and choose a macro from the dropdown menu.

:::image type="content" source="../../media/glint/setup/360-email-macros.png" alt-text="Screenshot of 360 macro options in a dropdown menu in the Welcome and Feedback Provider Selection email.":::

## Manage translations

Any edits made to 360 email text in English need to be made to all other survey languages. Use the guidance here to manage your email translations.

### Use the language dropdown

In the 360 email edit pane, after customizing English content, use the **Language** dropdown menu to select other survey languages and add translations to each survey section. Select **Save Changes** in the top right to save all of your edits.

:::image type="content" source="../../media/glint/setup/360-email-lang-dropdown.png" alt-text="Screenshot of the Language dropdown in the 360 email edit pane.":::

### Use the program content import

Use the [Viva Glint 360 cycle export and import option](360-export-import.md) to import updated translations for emails after modifying English text.

