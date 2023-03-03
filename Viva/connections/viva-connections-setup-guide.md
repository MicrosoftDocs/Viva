---
ms.date: 3/2/2023
title: Guide to setting up Viva Connections 
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
- intro-get-started
- highpri
ms.custom: intro-get-started
search.appverid:
- SPO160
- MET150
description: "Learn how to set up and launch Viva Connections for desktop and mobile devices"
---

# Set up and launch Viva Connections 

Microsoft [Viva Connections](viva-connections-overview.md) is an employee experience app in Microsoft Teams that brings together relevant news, conversations, and resources in one place for your organization. It's built on your current Microsoft 365 ecosystem to help you engage, inform, and empower your hybrid workforce. The Viva Connections experience is deployed and accessed in Microsoft Teams.

![Image of the Viva Connections desktop experience.](../media/connections/vc-full.png)

Use these step-by-step instructions to help you set up and launch Viva Connections on desktop and mobile devices to create an engaging user experience.

**In this guide, you’ll learn how to**

- Set up Viva Connections 
- Set up Viva Connections and a SharePoint home site
- Add a home site after setting up Viva Connections 

Follow the instructions that are relevant for your organization. If you are unsure if your organization has a [SharePoint home site](home-site-plan.md), ask your SharePoint admin. Home sites can be added after you’ve set up Viva Connections, but it’s recommended that you do it before to reduce the risk of needing to manually copy content in some cases. [Learn more about how Viva Connections and home sites work together to create employee experiences.](viva-connections-overview.md#how-sharepoint-home-sites-and-viva-connections-work-together) 

[Get more detailed guidance](viva-connections-setup-overview.md) that focus on tasks in the plan, build, and launch phases. Or, review the [Viva Connections learning path](/training/paths/viva-connections-get-started/) get more in-depth guidance that includes fictitious business stories, examples, and knowledge checks.


> [!IMPORTANT]
> - To complete these step-by-step instructions, ensure that you have permission to the SharePoint admin center (for customers who have a home site) and the Microsoft Teams admin center. Get more information about [permissions in SharePoint](/sharepoint/customize-sharepoint-site-permissions) and [permissions in Microsoft Teams](/microsoftteams/teams-channels-overview).
> - Viva Connections is not supported on the Linux operating system.
> - Viva Connections is not currently supported on tablet devices. Continue to check the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=) for the status of tablet support.


## Set up Viva Connections without a home site
Follow these instructions when your organization only wants to set up Viva Connections. 


### Step 1: Enable the Viva Connections app in the Microsoft Teams admin center  
Viva Connections does not have any requirements to get started. Start by adding the Viva Connections app, and then customize app settings to add your organization's logo, pre-install, and pre-pin the app for end users.

**Get started**
1.	[Add the Viva Connections app](add-viva-connections-app.md) in the Teams admin center (TAC).
2.	Then customize app settings like the app name and logo and decide user policies. Consider pre-pinning and pre-installing the app to improve app discoverability and adoption. 
3.	Finally, make the app available to end users by enabling the app.

**Permissions**
- Teams administrator (or higher) permissions are required to add the Viva Connections app to the Teams Admin Center (TAC).

### Step 2: Choose app settings  
The Viva Connections app creates a custom app in Microsoft Teams. Your organization’s custom app will appear as a branded company app in the Microsoft Teams app center. Once the app is added, your organization’s icon will appear in the Teams app bar in the desktop and mobile Microsoft Teams experience. Users won’t see the app by default if you don’t pre-install and pre-pin.

**Get started**
1.	If you have pre-pinned the app for your users with Teams app set-up policies in step 4, then the app will automatically appear in users’ Teams mobile client apps on iOS and Android.
2.	If you have not pinned the app via policy, then users will first need to search for and install Viva Connections from the Teams desktop application. [Learn more about Viva Connections settings](https://support.microsoft.com/office/choose-settings-for-the-viva-connections-mobile-app-61bc93fe-5d58-4b4c-a0b1-abdd484ccf46).

**Permissions**
- Teams administrator (or higher) permissions are required.

### Step 3: Assign owners and members 
Decide who should get access to editing elements of the landing experience. Assign at least 2 owners and a few members. If you are setting Viva Connections up for the first time, only owners of the SharePoint root site will be able to edit. When the home experience is edited for the first time, a SharePoint site on the backend will get created. You’ll want to assign (at least two) owners and members from this site to give permissions to others so they can edit the experience for the rest of the organization. [Learn more about what each role can do](edit-viva-home.md#manage-permissions).

**Get started**
1. Navigate to the Viva Connections app in Teams. 
2. Select the ellipsis (...) in the top-right and select **Manage permissions** and assign at least 2 owners and a few members. 
3. Alternatively, assign owners and members from the backend SharePoint site:

    - Select Edit in the dashboard section. 
    - Then select **Dashboard details**. 
    - Copy the link to the dashboard under **Properties > Name**. 
    - Paste the link in a browser and then go to **Settings > Permissions**. 



### Step 4: Finish customizing the experience 
After getting the app in Teams, choose the primary audience for this experience between employees who are generally frontline workers or information workers to select a set of default dashboard cards that can be edited or removed later. Add a custom banner image, add more cards to the dashboard (if desired), and set up navigational links to popular destinations in the navigation section. 

**Get started**
1. Learn more about [what content can be customized](edit-viva-home.md).
2. Upload a banner image, add more dashboard cards (if desired), and customize the navigation section. 

**Permissions**
- Member or owner permissions are required to change banner image, edit the dashboard, and edit navigational content.

### Step 5: Let your users know how to access and use Viva Connections

| Viva Connections dashboard interaction                 |End-user guidance                 | 
| :------------------- | :------------------- |
| ![Automated GIF of the Dashboard on a mobile device.](../media/connections/new-vc-dashboard-interaction.gif)  | Help make end users aware of this new resource and provide guidance on what icon in the Teams app bar is your organization's instance of Viva Connections. Then, help end users understand how to use [the desktop and mobile experiences](https://support.microsoft.com/office/your-intranet-is-now-in-microsoft-teams-8b4e7f76-f305-49a9-b6d2-09378476f95b). <br><br> [Learn more about how to help your organization adopt Viva Connections](https://adoption.microsoft.com/viva/). | 


## Set up a SharePoint home site and Viva Connections
Follow these instructions when your organization plans to use a SharePoint home site in combination with Viva Connections to create a complementary employee experience.

<br>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE53Exu]

<br>


### Step 1: Set a home site in SharePoint
A home site is a SharePoint communication site that acts as the front door to your organization’s intranet and has special capabilities such as the ability to prioritize news posted from the home site across the rest of the intranet. When you deploy Viva Connections, the SharePoint home site is automatically detected and a prominent link to the home site will display in the top-right corner of the Viva Connections experience. Alternatively, you can [choose to use the home site as the default landing experience](edit-viva-home.md#choose-the-default-landing-experience-for-viva-connections-desktop) if desired. 

> [!IMPORTANT]
> - Home sites are generally high-traffic sites that should be [optimized for performance](/sharepoint/portal-health).
> - Only modern SharePoint sites will open within the context of Microsoft Teams, classic sites, for example, will open in a separate browser window.

**Get started:**
1.	If your organization does not already have a home site, learn more about [how to plan a home site](home-site-plan.md) and [consider using this home site design](create-sharepoint-home-site-for-viva-connections.md).
2.	Then, [set the home site in the SharePoint admin center](/sharepoint/home-site).


**Permissions**
- SharePoint administrator (or higher) can set a home site.



### Step 2: Enable the SharePoint app bar and customize global navigation
The SharePoint app bar allows users to find important content, resources, and dynamically displays personalized sites, news, and files. Viva Connections uses elements from the SharePoint app bar and global navigation for desktop and mobile experiences. SharePoint app bar elements will display in Microsoft Teams and includes global navigation, followed sites, and recommended news. On mobile devices, Viva Connections uses global navigation for the **Resources** tab.

> [!IMPORTANT]
> - If your app bar is not set up, you won’t see a navigation links in the desktop experience, and global navigation resources in the Resources tab of the Viva Connections mobile app will not display.
> - A home site is required before you can enable and customize the SharePoint app bar.

**Get started**
1.	Learn more about [how to think about home site navigation and global navigation](https://techcommunity.microsoft.com/t5/video-hub/build-and-launch-a-sharepoint-home-site-tips-and-tricks-from-the/m-p/1696758).
2.	Learn how to [set up the SharePoint app bar and global navigation](sharepoint-app-bar.md).

**Permissions**
- Site owner (or higher) permissions to the home site are required to enable and customize global navigation in the SharePoint app bar.



### Step 3: Create your dashboard, add cards, and apply audience targeting in SharePoint
The dashboard brings it all together – it provides a personalized landing experience and is designed to be the central destination where everyone can discover your organization's resources and complete daily tasks. [Apply audience targeting to dashboard cards](use-audience-targeting-in-viva-connections.md) to give your users an experience tailored to their role and interests. Once you set up the dashboard, you will be able to use the [Dashboard web part on the home site](use-dashboard-web-part-on-home-site.md).

The dashboard can be set up and edited from the home site, or you can edit dashboard content in Teams from the Viva Connections desktop app.

**Get started**
1.	Learn how to [author your dashboard, add cards, and apply audience targeting](create-dashboard.md).
2.	*Optional* - Develop your own custom cards using [Adaptive Cards](/sharepoint/dev/spfx/viva/get-started/build-first-sharepoint-adaptive-card-extension).

**Permissions**
- Site member (or higher) permissions to the home site site are required to create and edit dashboard content.



### Step 4: Enable the Viva Connections app in the Microsoft Teams admin center
After you have prepared your home site, global navigation, and dashboard for Viva Connections in SharePoint, you are ready to add the Viva Connections app in the Microsoft Teams Admin Center. Add the Viva Connections app, and then customize app settings to add your organization's logo, pre-install, and pre-pin the app for end users.

**Get started**
1. [Add the Viva Connections app in the Teams admin center](add-viva-connections-app.md).
2. Then customize app settings like the app name and logo and decide user policies. Consider pre-pinning and pre-installing the app to improve app discoverability and adoption.
3. Finally, make the app available to end users by enabling the app.

**Permissions**
- Teams administrator (or higher) permissions are required to add the Viva Connections app to the Teams Admin Center (TAC).



### Step 5: Choose app settings 
The Viva Connections app creates a custom app in Microsoft Teams. Your organization’s custom app will appear as a branded company app in the Microsoft Teams app center. Once the app is added, your organization’s icon will appear in the Teams app bar in the desktop and mobile Microsoft Teams experience. Users won’t see the app by default if you don’t pre-install and pre-pin.

**Get started**
1. If you have pre-pinned the app for your users with Teams app set-up policies in step 4, then the app will automatically appear in users’ Teams mobile client apps on iOS and Android.
2. If you have not pinned the app via policy, then users will first need to search for and install Viva Connections from the Teams desktop application. [Learn more about Viva Connections mobile settings](https://support.microsoft.com/office/choose-settings-for-the-viva-connections-mobile-app-61bc93fe-5d58-4b4c-a0b1-abdd484ccf46).

**Permissions**
- Site member (or higher) permissions to the home site are required to choose settings for the mobile experience.


### Step 6: Finish customizing the experience 
After getting the app in Teams, finish setting up the experience by selecting a custom banner image. Viva Connections content can be edited from the Teams app and dashboard and navigational content can still be edited from the home site.

**Get started**
1. [Change the banner image in the header and set the focal point for the image](edit-viva-home.md#customize-the-banner-image). The banner image only displays in the desktop app.

**Permissions**
- Site owner (or higher) permissions to the home site are required to change the banner image.


### Step 7: Let your users know how to access and use Viva Connections

| Viva Connections dashboard interaction                 |End-user guidance                 | 
| :------------------- | :------------------- |
| ![Automated GIF of the Dashboard on a mobile device.](../media/connections/new-vc-dashboard-interaction.gif)  | Help make end users aware of this new resource and provide guidance on what icon in the Teams app bar is your organization's instance of Viva Connections. Then, help end users understand how to use [the desktop and mobile experiences](https://support.microsoft.com/office/your-intranet-is-now-in-microsoft-teams-8b4e7f76-f305-49a9-b6d2-09378476f95b). <br><br> [Learn more about how to help your organization adopt Viva Connections](https://adoption.microsoft.com/viva/). | 


## Add a SharePoint home site after setting up Viva Connections
Follow these instructions if your organization has already set up Viva Connections and now you want to add a home site. [Learn more about how Viva Connections and home sites work together to create employee experiences.](viva-connections-overview.md#how-sharepoint-home-sites-and-viva-connections-work-together) 


### Step 1: Set a home site in SharePoint
A home site is a SharePoint communication site that acts as the front door to your organization’s intranet and has special capabilities such as the ability to prioritize news posted from the home site across the rest of the intranet. When you deploy Viva Connections, the SharePoint home site is automatically detected and a prominent link to the home site will display in the top-right corner of the Viva Connections experience. Alternatively, you can choose to use the home site as the default landing experience if desired. 

> [!IMPORTANT]
> - If your app bar is not set up, you won’t see a navigation links in the desktop experience, and global navigation resources in the Resources tab of the Viva Connections mobile app will not display.
> - A home site is required before you can enable and customize the SharePoint app bar.

**Get started**
1.	If your organization does not already have a home site, learn more about [how to plan a home site](home-site-plan.md) and [consider using this home site design](create-sharepoint-home-site-for-viva-connections.md).
2.	Then, [set the home site in the SharePoint admin center](/sharepoint/home-site).


**Permissions**
- A SharePoint administrator (or higher) can create a home site.


### Step 2: Copy  content from the dashboard and navigation if needed
The home site will automatically be in draft mode so that content can be manually copied from the existing Viva Connections experience in Microsoft Teams if needed. 

After you’ve manually copied content (if needed) from the experience in Teams, turn the toggle off and select **Save** to activate the home site settings. Then, Viva Connections content will be sourced from the home site and can be edited either from the home site or the Viva Connections experience in Teams.

**Get started**
1.	Copy content (if needed) from the dashboard in Teams to the dashboard that can be found from the home site’s settings panel **Settings > Manage Viva Connections > Create dashboard**.
2. Copy content from navigation (if needed) to global navigation from the home site’s settings panel **Settings > Global navigation**. 


**Permissions**
- SharePoint site member permissions (or higher) to the home site can edit Viva Connections content from the home site and in Teams.


## Step 3: Publish the home site to share it with others
After you’ve finished setting up your home site and Viva Connections content in the dashboard and global navigation sections, publish the home site and share it with others to complete your organization's employee experience offering. After the home site has been published, the Viva Connections experience will automatically detect it and will display a link to the home site in the top-right corner.

**Get started:**
1.	Consider running a [health check](/sharepoint/portal-health) to ensure site performance for a high-traffic site.
2.	Add the intended audience to the **Settings > Site permissions** as site viewers.
3.	[Share the site](https://support.microsoft.com/office/share-a-site-958771a8-d041-4eb8-b51c-afea2eae3658) with the intended audience.

**Permissions**
- SharePoint site member permissions (or higher) to the home site can publish the home site and add site visitors.




## Learn more

[Overview of Viva Connections](viva-connections-overview.md)

[Customize and edit the Viva Connections home experience](edit-viva-home.md)

[Microsoft Viva adoption center](https://adoption.microsoft.com/viva/)
