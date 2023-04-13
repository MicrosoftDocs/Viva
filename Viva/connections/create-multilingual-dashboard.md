---
ms.date: 3/1/2023
title: "Create a Viva Connections dashboard in more than one language"
ms.reviewer: 
ms.author: hokavian
author: Holland-ODSP
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
localization_priority: Priority
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-connections
search.appverid:
- SPO160
- MET150
description: "Learn how to create a Viva Connections dashboard in more than one language"
---

# Create a Viva Connections dashboard in more than one language

Create a Viva Connections dashboard that can be viewed in multiple languages. Start by enabling the multilingual experience, select languages, and then assign translators. 

>[!NOTE] 
> You must have member level permissions or higher to edit multilingual settings.


## Step 1: Navigate to the Viva Connections dashboard

Depending on whether your organization has a [SharePoint home site](home-site-plan.md) or not will determine where you go to access the multilingual settings.

**If your organization has a home site:**
1.	Navigate to your organization’s home site in SharePoint.

**If your organization doesn’t have a home site:**
1.	Navigate to the Viva Connections app in Teams.
2.	Select **Edit** in the dashboard section.
3.	Then select **Dashboard details**.
4.	Copy the link to the dashboard under **Properties > Name**.
5.	Paste the link in a browser and then go to **Settings** in the top-right corner.


## Step 2: Enable the multilingual experience and choose languages in Site settings
1.	Select **Settings** from the top right, and then select **Site information**.
2.	At the bottom of the site information pane, select **View all site settings**.
3.	Under **Site Administration**, select **Language settings**.

     ![Image of multilingual settings in the advanced settings panel.](../media/connections/viva-language-enable.png)

4.	Under **Enable pages and news to be translated into multiple languages**, slide the toggle to **On**.

## Step 3: Select languages and assign translators
1.	Under **Add or remove site languages**, start typing a language name in **Select or type a language**, or choose a language from the dropdown. You can repeat this step to add multiple languages. You can add or remove languages from your site at any time by going back to this page.
2.	In the **Translator** column, start typing the name of a person you want to be a [translator](https://support.microsoft.com/office/create-multilingual-communication-sites-pages-and-news-2bb7d610-5453-41c6-a0e8-6f40b3ed750c?ui=en-us&rs=en-us&ad=us#bkmk_translators), and then select the name from the list.


     ![Image of multilingual settings turned on.](../media/connections/viva-setting-language.png)


3. Select **Save**.


>[!NOTE] 
> - Anyone in your organization's [Active Directory](/azure/active-directory/fundamentals/active-directory-whatis) can be assigned as a translator. People assigned as translators will not automatically be given appropriate permissions. When someone without edit permissions to the dashboard tries to access the site, they will be directed to a web page where they can request access.
> - You can add or remove languages from your dashboard at any time by going back to this settings page.
> - The default language of a dashboard is set to the language chosen when the dashboard is created. However, when English is among the supported languages, English is treated as the preferred language if the user's preferred language is not supported by the dashboard. This is a known issue.


## Step 4: Create dashboards in specific languages
Translators manually translate copies of the dashboard into the language(s) specified. When you select a language and assign a translator, a copy of the dashboard is created, and translators are notified in an email that a translation is requested. The email includes a link to a copy of the dashboard. An email notification will be sent to the person who requested the translation when it's done. The translator will:

1.	Select the **Start translating** button in the email.

     ![Image of a email translation request.](../media/connections/ml-dashboard-email.png)

2.	Select **Edit** on the top right of the dashboard and translate the content.

3.	When the translation is done, select **Save as draft** (if you're not ready to make it visible to readers) or, if the dashboard is ready to be visible to everyone who is using that language on the site, select **Publish**.


>[!NOTE] 
> Some components of 2nd and 3rd party Dashboard cards (for example, the card name) may not be translatable. 


## Step 5: Add a translated dashboard name and description

1.	To edit the description, from the dashboard, select **Dashboard settings** in the command bar.
2.	**Edit** the dashboard description.
3.	To edit the name of the dashboard, navigate to **Settings**, and then **Site contents**, and then find the translated dashboard in **Site pages**. Hover over the dashboard that you want to rename and select the ellipsis **(...)** and then select **Rename.**


## Email notifications
Learn more about when and why the default dashboard owner and assigned translators will receive emails when content is edited.

Email notifications are batched in 30-minute increments as needed. For example, when the first email related to a page is sent, and an update is made to the default language page, the next notification email or any others that need to be sent, will be batched, and sent after 30 minutes.

- When a translation dashboard is created, an email is sent to the assigned translator(s) to request a translation. The email includes a Start translating button.


- When a translation dashboard is published by a translator, an email is sent to the person who requested the translation.
- When an update is made to the default language dashboard and saved as a draft or is published, an email is sent to the translator to notify them that an update to the translation dashboard may be required.



## More tasks for your multilingual dashboard
After you’ve created dashboards in additional languages, learn more about how to confirm which languages are available, update translated versions, and delete translations that are no longer needed. 

### Confirm the languages the dashboard can be viewed in
The status of the translation of the dashboard (draft saved, published, and so on) is shown in the Translation pane next to each language. To see the status:

 
1.	Go to the default dashboard.
2.	Select **Translation** at the top of the page.
3.	In the Translation pane on the right, the status of each language is shown, as well as a link to view the dashboard in that specific language.


### Find a translated dashboard
You can use the language dropdown at the top of the page, the translation panel, or find the dashboard in the Pages library.


To find it in the Pages library, do this:

1.	Go to the Pages library for the home site.
2.	Find the dashboard you want to delete in the language folder adjacent to the default language page. The folder can be identified by its 2- or 4-letter language code. For example, the French folder will be identified as "fr."


### Delete a version of the dashboard for a specific language
To delete a translated dashboard, you must perform a few additional steps to break the association between the default language dashboard and the deleted dashboard.
1.	Go to the **Pages library** for the dashboard.
2.	Find the version of the dashboard you want to delete in the language folder adjacent to the default language page. The folder can be identified by its 2- or 4-letter language code. For example, the French folder will be identified as "fr."
3.	Select the dashboard you want within the folder, and then select the ellipsis (...) to the right of the selected page.
4.	Select **Delete**.
5.	After you've deleted the version of the dashboard that’s no longer needed, go to the default language dashboard, and select **Edit** at the top right. If you are not in edit mode, the rest of the steps will not work.
6.	Select **Translation** at the top of the page.
7.	In the Translation panel, you should see a message indicating that an association with the page has been removed.
8.	**Republish** the default language dashboard.


### Update the dashboard with new changes or edits
Make changes as needed over time to the dashboard and select **Save as draft** or **Republish**. Then, the translator(s) for the translated dashboard are notified in email that an update has been made so updates can be made to the individual translation pages as well.

### Update the default language page
When the default language dashboard is updated, it must be republished. Then, the translator(s) for the translated dashboard are notified in email that an update has been made so updates can be made to the individual translation pages. Translators will need to view the version history of the default dashboard to see what content has changed.


## Translated dashboards in the Dashboard web part
The [Dashboard web part](/sharepoint/use-dashboard-web-part-on-home-site) can be used once the dashboard has been published. The Dashboard web part will display in the users preferred language (if different from the default language) if a translated dashboard has been provided.
Note: 
 - Translation dashboards must be approved and published before they will appear.
 - Some components of the 2nd party and 3rd party dashboard cards (like the card name) may not be translatable. 


 ### More resources

[Set up the Viva Connections experience in a specific language](/viva/connections/viva-connections-language)

[Edit the Viva Connections dashboard](/viva/connections/create-dashboard)

[Create multilingual communication sites, pages, and news](https://support.microsoft.com/office/create-multilingual-communication-sites-pages-and-news-2bb7d610-5453-41c6-a0e8-6f40b3ed750c)

