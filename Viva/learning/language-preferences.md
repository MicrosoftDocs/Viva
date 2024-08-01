---
title: Language preferences in Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 06/28/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: Manage your language settings in Viva Learning for users across Teams, webapp and mobile. 
---

# Language preference settings

Manage Viva Learning language settings for users across Teams, the web app, and mobile. We recommend you set up all language settings as the initial step of Viva Learning onboarding process or pilot phase.

## Access

Admins with access to Admin Tab in Viva Learning are able to view and edit the setting.

## Default language 

Default language is the setting that informs Viva Learning of a more relatable language for the Tenant. It's used as a fallback when Viva Learning can't resolve a language. 

Admins can choose from over [60 supported languages](/viva/learning/viva-learning-supported-languages) as the Viva Learning default language. The default language is a required setting, with English (United States) as the preset.  

### Impacted features of default language

Some places where default language is used: 

- When tenants select the [second language setting](#displaying-content-in-default-and-user-selected-languages)
Learners see learning content from both display and default language. 

- Sharepoint object with a null/empty `ContentLanguage` field are defaulted to default language.
 
- Fall back process of deciding the language of the user for Assignments 

- Available languages setting

- User language setting  

Updates to **Show Learning content in default and user-selected languages** take an hour and updates to Available Language take 24 hours. Hence, updates to default language take applicable time to reflect in their impact spaces.

Changes to default language setting will be visible immediately for other features after.

### Guidelines for choosing default language

The default language is chosen based on any or all these parameters:

1. The language that most of the learning content is created

1. The language that most users prefer or use


1. The operating language of the tenant

> [!NOTE]
>
>- The default language is applicable and used only in Viva Learning context. It doesn't impact any other Viva or Microsoft products or spaces.
>- The default language doesn't override the user language. The default language is used as a fallback and displaying content along with user language.
>- Default language application in Viva Learning features like assignments, notifications, and skills are scheduled for upcoming releases.
>- RTL languages cannot be added as a default language as Viva Learning does not support RTL languages. Any previously added RTL language as the default language will be updated to English (United States).

## Displaying content in default and user-selected languages

Viva Learning displays Learning content from the user-chosen language ([display language](/viva/learning/language-overview/#display-language)) and default language (settings above). This avoids a situation where the user doesn't receive any learning content.

If an admin wants Viva Learning to load only in the user-chosen language, they can switch off the **Show Learning content in default and user-selected languages** setting. 

### Impacted spaces


When switched off, users can only see content pertaining to their selected language in the following spaces:

- **Home** Page of Viva Learning
  - **Interests** section
  - **Browse by** section
- **Search result** page and all search modals
- **Suggestions** in learning content details view

When **Show Learning content in default and user-selected languages** is switched on, users can see content from both user-chosen language and the default language in the spaces mentioned. This setting is switched on by default.

Spaces and pages not mentioned aren't impacted by this setting.

Updates to this setting may take up to an hour to reflect to all users of Viva Learning after confirmation. 

> [!NOTE]
> If the **Show Learning Content in Default and User-selected Languages** is switched off, users may experience Viva Learning with no learning content. SharePoint objects and learning paths created by admins may also not be visible to the user as the user-chosen language may be different from the language of creation.

## Available languages 

Admins can set all the supported languages that the organization supports in Viva Learning. Available language has two options to choose from:

- All supported languages in Viva Learning -   selects [all languages supported by Viva Learning](/viva/learning/viva-learning-supported-languages).
  - By default, this option is selected. Viva Learning default language chosen above can't be removed. 
- A subset of specific languages - provides an option for the admin to select a specific list of languages.

### Impacted features of available languages


Any changes to languages in **Available Languages** setting modify the filter options of the language filter and options in **User Language setting**.

Changes may take up to 24 hours to reflect for all users after confirmation. Users may clear browser cache and local storage to see the change immediately.

### Guidelines for choosing available languages 

Select the languages that satisfy either one or all the below criteria:

- Languages in which learning content is made

- Languages which employees understand/interested in learning from

- Operating languages of the tenant

> [!NOTE]
> 
> Available languages will be used in Skills feature in the upcoming releases. 

## User language

> [!NOTE]
> 
> User language is currently in private preview. Please check with your Microsoft representative to participate in private preview. 

All Viva Learning Users can select their Viva Learning Language independent of the Teams/Browser's language. Users can access their language setting: Viva Learning App -> Three dots in top right of Header -> Settings -> Language -> Choose a Language -> select "Save & Refresh". Languages selected in the **Available Languages** setting will be shown in the options of User Language Settings.

User language setting persists across different surfaces - Teams and Browser - for the user. At any point in time, if a tenant removes support for a language, and a user tries to access Viva Learning in that language then Viva Learning opens in Viva Learning default language and the user is notified about it.

### Day 0 experience

When a user accesses Viva Learning for the first time, the user language is preselected by default as per the language of their Teams or browser. If the Teams or browser languages aren't supported by the tenant, then Viva Learning opens in the Viva Learning default language and the user is notified about it.

> [!NOTE]
> 
> Viva Learning Mobile App opens in the Language of the mobile device. User Language support in mobile will be done in the upcoming releases.
