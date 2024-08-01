---
title: Customize Viva Glint survey email content
description: Customize Microsoft Viva Glint email content for survey invites, reminders, and survey results notifications in the Communications section of Program Setup.
ms.author: aweixelman
author: AliciaWeixelman
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: email, reminder, invite, custom email, results notification
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 07/09/2024
---

# Customize Viva Glint survey email content

Customize Microsoft Viva Glint email content for survey invites, reminders, and survey results notifications in the Communications section of Program Setup. Optionally, set up a custom email sending domain and a company logo for survey emails. To understand how to enable/disable emails, and for more information about Communications setup, see [Communications setup in Program Summary](program-summary-communications.md).

> [!IMPORTANT]
> Always-On survey programs don't include emails or a Communications section.

## Custom sending domains and themes/logos (optional)

In the [Microsoft Admin Center (MAC)](https://go.microsoft.com/fwlink/?linkid=2264234), your M365 admin can optionally configure a custom sending domain for your organization. In the [Microsoft Entra admin center](https://entra.microsoft.com/#home), customize your organization's branding to include your logo in survey communications:

- [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products)
- [Customize company branding](/entra/fundamentals/how-to-customize-branding)
  - To add your organization's logo to Viva Glint survey emails, set up the **Sign-in form** > **Banner logo** in the Microsoft Entra admin center.

Both items are **optional steps** that your organization can take to further customize the survey
communication experience for your survey participants.

> [!NOTE]
> - Custom sending domains configured in MAC can impact other M365 products. See [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products) for a full list.
> - Viva Glint teams have access to limited email delivery metrics. Using a custom sender domain gives your organization direct access to your email delivery data.

## Email sections

To edit email content, go to the Communications section of your desired survey program, select the pencil icon to edit a given email, and in the edit pane that appears, select the pencil icon to edit content.

Viva Glint survey invites and reminders contain multiple editable sections:

:::image type="content" source="../../media/glint/setup/glint-email-invite-sections.png" alt-text="Screenshot of editable survey email sections in Viva Glint.":::

The following invite and reminder email sections support multiple paragraphs to break up and emphasize important text:

- Message
- Privacy Message

Add your customizations to each section and select **Save Changes** in the top right to save all of your edits.

> [!CAUTION]
> Hyperlinks and HTML aren't supported content in Viva Glint customized emails. These items can cause email delivery/blocking issues.

### Email macros

Macros in Viva Glint emails allow your organization to add placeholders that pull in information from your employee data and from Viva Glint. Include Departments, Manager Names, or estimated minutes to complete a survey in email text to further customize for survey participants. To add a macro, select the plus sign icon email sections where it exists and choose a macro from the dropdown menu.

:::image type="content" source="../../media/glint/setup/glint-email-macros.png" alt-text="Screenshot of macros available to add to email text.":::

## Manage translations

Any edits made to email text in English need to be made to all other survey languages. Use the guidance here to manage your email translations.

### Use the language dropdown

In the email edit pane, after customizing English content, use the **Language** dropdown menu to select other survey languages and add translations to each survey section. Select **Save Changes** in the top right to save all of your edits.

:::image type="content" source="../../media/glint/setup/glint-email-language-dropdown.png" alt-text="Screenshot of the Language dropdown in the email edit pane.":::

### Use the program content import

Use this [translation guidance](language-translations.md) to import updated translations for emails after modifying English text.

## Survey End Results Notification email

The Survey End Results Notification email is designed to notify managers that their results are ready for review in Viva Glint dashboards. It contains several sections, including some that link to additional resources. 

Sections that can be easily customized: 

- Button Text
- Greeting
- Main Title
- Preview Text
- Subject
- Title
- Tip Titles
- Tip Descriptions

Sections to avoid customizing:

- Links
- Icons

The following results notification email sections support multiple paragraphs to break up and emphasize important text:

- Description
- Main Title
- Tip 1 Description
- Tip 2 Description
- Tip 3 Description

:::image type="content" source="../../media/glint/setup/glint-survey-results-notification.png" alt-text="Screenshot of the Survey End Results Notification email.":::

## Preview emails

After customizing emails, use the Viva Glint [preview option](preview-manage-enable-engage-programs.md) to send yourself a sample email.

> [!TIP]
> For email previews in other languages, select a 'preview as' user that's assigned the language code that you want to see a preview for. Learn more in the **Language** section in [Viva Glint employee attribute fundamentals](attribute-fundamentals.md).

> [!NOTE]
> - To allow for easier email review, email previews for surveys that require authentication via Entra don't include an Entra link behind the Provide Feedback button.
> - Preview emails can only be sent for survey invites. Reminders and survey results notifications can be previewed in the editing pane in the platform.
