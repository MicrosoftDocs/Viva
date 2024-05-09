---
title: Overview of language in Viva Language 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 06/08/2023
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: Learn how Viva Learning handles language so you can customize the application.
---

# Overview of Language in Viva Learning

Learn how Viva Learning handles language so you can customize the application.

## Introduction

Viva Learning follows international guidelines in language field of all learning content.

The language field has two parts: `ab-CD`  
“ab” represents language as per ISO 639-1 format and “CD” represents locale/country code as per ISO 3166 format.

For example, English used in the United States is shortened as `en-US`.

Language in used in two areas within Viva Learning:

1. **Display language**: The language in the app, including navigation elements and notifications

2. **Content language**: The language of the learning content hosted within Viva Learning

For more information, review the list of Viva Learning [supported languages](/viva/learning/viva-learning-supported-languages).


## Display language

Display language refers to the language in which Viva Learning is accessed. It refers to the language that the navigation names display. This includes **Home**, **My Learning**, and **Manage**, as well as actions like **Share**, **Add to calendar**, and **Rate it**. Notifications in Teams also display in the same language. 

### In the Teams app or web app

When using Viva Learning in Microsoft Teams or in the Browser. Viva Learning display language is set through the Language setting within Viva Learning.

Open Viva Learning app > Select the three dots on the top right in header. Then go to **Settings** > **Language** > **Select a Language > Save & Refresh**. 

> [!NOTE]
> User language is currently in private preview. Languages shown in Language setting in Viva Learning are as per the [Available language setting](/viva/learning/language-preferences/#available-languages). To add or modify the language options, use the available language setting. 
> If you're not participating in the User language private preview, the display language defaults to the Microsoft Teams or browser language.
## Content language

Content language refers to the language of the learning content in Viva Learning.

By default, learning content is loaded in two languages: the [display language](#display-language) and the [default language](/viva/learning/language-preferences/#Default-language).

Learning content is loaded in two languages to avoid the “no learning content” experience. Admins can disable this experience through the [Language preference](/viva/learning/language-preferences/#displaying-content-in-default-and-user-selected-languages) settings.

Learning content in two languages is only visible in the following spaces:

- **Home** page of Viva Learning:
  - **Interests** section
  - **Browse by** section
- **Search result** page and all search modals
- **Assignments** in the **My Learning** tab (Refer to FAQ)
- **Admin** tab
- **Suggestions** in the learning content details view
- **Compose Extension** in Teams Chat
- **Social** tabs in Teams Chat

The following spaces display content only based on user action or preference. They don't show content from two languages.

- **My Learning** tab
  - **Recommendations**
  - **Bookmarks**
  - **In progress**
  - **Collections**
  - **Completed**
- **Trending** section in the **Home** page
- **Manage** tab
- **Share** and **Recommend** actions

## FAQs

- **Why does Viva Learning show English content at all spaces even if my Viva learning language is not English?**

    By default, Viva Learning shows content from two languages: the display language and **English (US)**(default language).

    If the admin doesn't want this experience, it can be modified in the [Language preference](/viva/learning/language-preferences/#Displaying-content-in-default-and-user-selected-languages) settings.

- **My learning content is available only in language code format (en,fr,es – no country code). How does Viva Learning handle such content?**

    A language with only a language code is called a neutral language. Viva Learning implicitly supports neutral languages in display and default languages.

    For example, if a user is using Viva Learning in Deutsch (Deutschland) – (de-DE), Viva Learning loads all content having language attribute as either (de-DE) or (de).
    
 - **Viva Learning is loading in a different language in PC and mobile device. Is it expected?**
 
    Viva Learning in mobile will open as per language of the mobile device. User Language setting will be implemented for mobile in the upcoming releases.

 - **We are not able to see a specific language content of a provider or LMS.**
    
    Check the documentation of each provider integration to know the supported languages or reach out to the support executive to know the supported languages in each provider or LMS.

- **In which language are assignments shown to users in Viva Learning?**

    The language of assignments is set as follows: **Display language** > **English (US)**

    The assignment is loaded in the display language of the User. If the assignment isn't available in display language, then it's loaded in English (US).  We are working on including Default language in this fallback process. 


