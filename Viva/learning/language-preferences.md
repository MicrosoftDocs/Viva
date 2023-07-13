---
title: Language preferences in Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 07/11/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: medium
description: Manage your language settings in Viva Learning for users across Teams, webapp and mobile. 
---

# Language preference settings

Manage Viva Learning language settings for users across Teams, the web app, and mobile. We recommend you set up all language settings as the initial step of Viva Learning onboarding process or pilot phase.


> [!NOTE]
> Language settings is under private preview. Please check with your support executive to participate in the private preview.

## Access

Admins with access to Admin Tab in Viva Learning will be able to view and edit the setting.

## Default language 

Admins can choose from over [60 supported languages](/viva/learning/viva-learning-supported-languages) as the Viva Learning default language.

The default language is a required setting, with English (United States) as the preset.  


Some places where Default language is used: 

- When tenants select the [second language setting](#displaying-content-in-default-and-user-selected-languages)
Learners see learning content from both display and default language

- Sharepoint object with a null/empty `ContentLanguage` field will be defaulted to default language.

Updates to default language setting are visible immediately to all users of Viva Learning in the tenant after editing.

### Guidelines for choosing default language

The default language is chosen based on any or all of these parameters:

1. The language that most users prefer or use

1. The language that most of the learning content is created

1. The operating language of the tenant

> [!NOTE]
>
>- The default language is applicable and used only in Viva Learning context. It doesn't impact any other Viva or Microsoft products or spaces.
>- The default language doesn't override the user language. The default language is used as a fallback and displaying content along with user language.
>- Default language application in Viva Learning features like assignments, notifications, and skills are scheduled for upcoming releases.

## Displaying content in default and user-selected languages

Viva Learning displays Learning content from the user-chosen language ([display language](/viva/learning/language-overview/#display-language)) and default language (settings above). This avoids a situation where the user doesn't receive any learning content.

If an admin wants Viva Learning to load only in the user-chosen language, they can switch off the **Show Learning content in default and user-selected languages** setting. 

When switched off, users can only see content pertaining to their selected language in the following spaces:

- **Home** Page of Viva Learning
  - **Interests** section
  - **Browse by** section
- **Search result** page and all search modals
- **Suggestions** in learning content details view

When **Show Learning content in default and user-selected languages** is switched on, users can see content from both user-chosen language and the default language in the spaces mentioned above. This is switched on by default.

Spaces and pages not mentioned above aren't impacted by this setting.

Updates to this setting reflect immediately to all users of Viva Learning after editing.

> [!NOTE]
> If the **Show Learning Content in Default and User-selected Languages** is switched off, users may experience Viva Learning with no learning content.
Sharepoint objects and learning paths created by admins may also not be visible to the user as the user-chosen language may be different from the language of creation.
