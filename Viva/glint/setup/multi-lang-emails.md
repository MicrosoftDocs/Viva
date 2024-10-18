---
title: Use multiple languages in Viva Glint survey emails
description: To ensure that your global employee population receives communications that they can understand, use emails with two or three unique language sections in Microsoft Viva Glint.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: multi-language, multiple language email, email translations
ms.collection:  
- Microsoft 365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/26/2024
---

# Use multiple languages in Viva Glint survey emails

To ensure that your global employee population receives communications that they can understand, use emails with two or three unique language sections in Microsoft Viva Glint. Use cases include:

- Adherence to local guidelines that require organizations to communicate in multiple languages.
- Unreliable language preference information in employee data.

> [!NOTE]
> - Multiple language emails: 
>   - are for survey communications only and aren’t supported for Team Conversations emails.
>   - don't currently support right to left languages.
>   - aren't currently editable with the [export/import email content feature](language-translations.md) and translations must be added directly in email fields in the platform.

## How multiple language emails work

Standard Viva Glint survey emails include a single language that can be triggered based on a language code on the employee data you upload to Glint. Multiple language emails (dual and triple) allow your organization to include sections in multiple languages in one survey email.  

### Dual language emails

For dual language emails, each language that you select for a survey is tied to an email that includes two language sections. For example, users coded for Spanish (Latin America) could see an email with English and Spanish sections: 

:::image type="content" source="../../media/glint/setup/dual-lang-preview.png" alt-text="Screenshot of an email preview for a dual language email with sections in Spanish and English.":::

### Triple language emails

You may want to use triple language emails to send users survey emails that contain three languages so that participants can choose the correct survey language from their invites and reminders:

:::image type="content" source="../../media/glint/setup/three-lang-preview.png" alt-text="Screenshot of an email preview for a triple language email with sections in English, Spanish, and French.":::

### Survey start buttons

In dual and triple language emails, when a survey participant selects a Provide Feedback button in any language section:

- They land on the survey welcome page in the survey language code tied to their user profile. Participants can select a different language from the dropdown menu.
- They land on the survey welcome page in the default survey language when there's an invalid or blank language code tied to their user profile. Participants can select a different language from the dropdown menu.

### Language selection links

To let users jump to a language section in multiple language emails, use the Select Language field during email setup. Add the name of the language that should be selected. For example, in this dual language email, to have Spanish (Latin America) users see a Select Language option that takes them to the English section of the email, add "English" to the Select Language field:

:::image type="content" source="../../media/glint/setup/multi-lang-select-lang-setup.png" alt-text="Screenshot of an email setup pane with English populated in the Select Language field.":::

With this setup, Spanish (Latin America) users see this language selection option at the top of multiple language emails which lets them quickly skip to the English section of the email:

:::image type="content" source="../../media/glint/setup/multi-lang-select-lang.png" alt-text="Screenshot of an email with Spanish and English sections and a Select Language hyperlink at the top of the email.":::

### Confirm that your organization uses a language attribute

To use Viva Glint survey emails that contain sections in different languages, your organization needs to use a survey language attribute. [Learn more](https://go.microsoft.com/fwlink/?linkid=2275842).

## Enable multiple languages for emails

To enable multiple language sections in emails for survey participants:

1. From the admin dashboard, select **Configuration** and then choose **Survey Programs**.
1. Select a survey and go to the **Communications** section.
1. In **Email Settings**, switch on the **Show multiple languages for recipient in certain locale** toggle.
2. In the dropdown menu that appears, select Dual Language Survey/Reminder or Triple Language Survey/Reminder.
3. Select **Save Changes** in the top right of the **Communications** page.

   :::image type="content" source="../../media/glint/setup/email-settings-multi-lang.png" alt-text="Screenshot of the multiple language email setting in the Communications section of survey setup.":::
   
## Configure dual language emails

After enabling multiple languages and selecting **Dual Language Survey/Reminder** for emails: 

1. In dual language emails, in addition to usual email fields, there are **(Local Language)** sections that appear.
1. Select each option from the **Language** dropdown menu. Add content to the standard email fields and second language translations to the **(Local Language)** sections.
2. For example: To send users coded for Spanish (Latin America) an email that includes English and Spanish (Latin America), select Spanish (Latin America) from the dropdown menu and populate fields like this image:

   :::image type="content" source="../../media/glint/setup/edit-dual-lang.png" alt-text="Screenshot of a dual language email edit pane with English and Spanish content added.":::

   1. For users to receive this email, they need to be coded for Spanish (Latin America) (es_US) in employee data uploaded to Glint.
   1. Users with blank or invalid language values receive the email that’s configured in your organization’s default language (often English).
2. After adding all content in each language, select **Save Changes**.

> [!TIP]
> (Local Language) sections aren’t auto populated with translations in dual language emails. For customized text, add customized translations. For Glint standard text, export translations from another survey program without multiple language emails to use as a reference.

## Configure triple language emails
   
After enabling multiple languages and selecting **Triple Language Survey/Reminder** for emails:

1. Select the pencil icon next to the survey invite or reminder that you want to edit.
2. In triple language emails, in addition to usual email fields, there are **(Language 2)** and **(Language 3)** sections that appear.
3. Select each option from the **Language** dropdown menu. Add content to the standard, Language 2, and Language 3 versions of the email sections.
4. For example: To send all users an email that includes English, Spanish (Latin America), and French, you can select English from the dropdown menu and populate fields like this image:

   :::image type="content" source="../../media/glint/setup/three-lang-edit.png" alt-text="Screenshot of a triple language email edit pane with English, Spanish, and French content added.":::

   1. For users to receive this email, they need to be coded for English (en_US) in employee data uploaded to Glint.
   1. Users with blank or invalid language values receive the email that’s configured in your organization’s default language (often English).
7. After adding all content in each language, select Save Changes.

> [!TIP]
> Language 2 and Language 3 sections aren’t auto populated with translations in triple language emails. For customized text, add customized translations. For Glint standard text, export translations from another survey program without multiple language emails to use as a reference.

## Preview survey invites

Use Viva Glint’s preview option to send yourself a sample survey invite: [Learn more](https://go.microsoft.com/fwlink/?linkid=2276910).

> [!TIP]
> To preview multi-language email invites connected to each language that you added content for, select a 'preview as' user that's assigned the language code that you want to see a preview for. For example, to preview a Spanish (Latin America) email that contains English and Spanish sections, select a user assigned the Spanish (Latin America) language code: es_US.
