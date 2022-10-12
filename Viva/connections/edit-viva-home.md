---
title: "Customize and edit the Viva Connections home experience"
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
- highpri
search.appverid:
- SPO160
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: "Learn how to customize and edit the Viva Connections home experience"
---

# Customize and edit the Viva Connections home experience

The new [Viva Connections](viva-connections-overview.md) desktop design serves as a new home experience option that centers essential job tasks, personalized content, easy access to other Viva experiences, and better aligns with the mobile experience. [Learn more about the new Viva Connections home experience](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/more-options-coming-soon-for-the-viva-connections-desktop/ba-p/3644419). 

Elements of the new Viva Connections home experience can be customized to fit your organization’s brand and the needs of your end users. Learn more about how to customize the banner, Dashboard content, and navigational links in Resources. Then, learn how to influence content in the Feed. Finally, learn how to manage access and permissions. 

>[!NOTE]
> - The new Viva Connections home experience will be available for [Targeted release](/microsoft-365/admin/manage/release-options-in-office-365) customers by the end of November 2022 and will become generally available to all customers in 2023.
> - If you already have Viva Connections set up, the new home design uses current content and settings (like audience targeting) from your Dashboard and Resources and there will not be any impact to the mobile experience. 
> - If your organization has a home site, you can choose to use it as the default home experience. The ability to choose the default experience will become available when the feature rolls out in November. More details will be shared soon.
> - If you haven’t set up Viva Connections yet, the default experience includes cards on the Dashboard but otherwise doesn’t impact [the mobile experience](/viva-connections-overview.md#the-viva-connections-mobile-experience).
> - The new home experience uses a similar permission model to SharePoint and can be managed from Microsoft Teams. 
> - You must have member level permissions or higher to edit the new desktop experience.

## About the new Viva Connections home experience

The home experience focuses on the top tasks, tools, and resources that help people in your organization get their jobs done. The new design prominently features key elements to the [Viva Connections experience](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0) - the Dashboard, Feed, and Resources. Content in these elements is filtered [using audience targeting to create a personalized experience](use-audience-targeting-in-viva-connections.md). 

![Image of the full page home experience.](../media/connections/vc-full.png) 

**Dashboard:** [The Dashboard](/viva-connections-overview.md#viva-connections-dashboard) is your employee’s digital toolset. It brings together the tools your employees need, enabling quick and easy access whether they are in the office or in the field. 

**Feed:** [The Feed](/viva-connections-overview.md#viva-connections-feed) delivers updates to the right people at the right time and is tightly integrated with Yammer, SharePoint news, and Stream to display a personalized feed, based on post-level targeting of the groups that employees belong to. 

**Resources:** [The Resources](/viva-connections-overview.md#viva-connections-resources) experience enables navigation across portals and destinations.

 **Navigational elements:** Located in the top-right and top-left corners, [navigational elements](https://go.microsoft.com/fwlink/?linkid=2208247) help viewers easily get to-and-from other landing pages and [other Viva experience](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0).

### Summary of customizable elements 

![Image of the full page home experience with labels that explain which parts can be edited.](../media/connections/vc-edit-1.png)  

1. **App icon and label in the Teams app bar:** Customize the app name and label in the [Teams admin center](add-viva-connections-app.md). 

2. **Banner image:** Upload a banner image and set the focal point to create a branded look. 

3. **Entry point to secondary landing page:** A link to the preferred default desktop experience will automatically display here. 

4. **Dashboard:** Customize with [cards and content](create-dashboard.md) specific to roles, regions, departments, and popular tasks. 

5. **Resources:** Add navigational links and labels in the first column of the Resources section. Content in Frequent and Followed sites are dynamically displayed based on the viewers interests and activity. 

### Summary of non-customizable elements 

![Image of the full page home experience with labels that explain which parts can be further edited.](../media/connections/vc-edit-2.png)  

6. **Shared Viva navigation:** Helps viewers navigate between Viva experiences. Viva apps will automatically display in this menu when Viva licenses are detected. 

7. **Ellipses menu:** Access more information about the home experience depending on your level of permissions. 

8. **Viva navigational bar:** This provides an opportunity to discover [more Viva experiences](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0) and gets automatically generated when Viva licenses are detected. 

9. **Feed:** Content in the Feed is dynamically generated based on the sites and communities the user follows. [Learn more about how content in the Feed is sourced](/faqs-viva-connections-feed). 

10. **Frequent sites and Followed sites:** Content in these sections is dynamically displayed based on the viewers interests and activity. 

## Get started customizing the experience

>[!NOTE]
> - You must have member level permissions (or higher) to edit the new desktop experience.
> - If your organization has a home site, you can choose to use it as the default home experience. The ability to choose the default experience will become available when the feature rolls out in November.

### How to edit the Viva Connections desktop experience for the first time

If you already have Viva Connections setup, editors who have site owner or member permissions to the home site will automatically have owner or member permissions to the new home experience in Teams. People with member permissions or higher will automatically see **Edit** buttons in the home experience.

If you are setting it up for the first time, only owners of the SharePoint root site will be able to edit. When the home experience is edited for the first time, a SharePoint site on the backend will get created. You’ll want to assign (at least two) owners and members from this site to give permissions to others so they can edit the experience for the rest of the organization. Manage permissions from the backend site by going to **Settings > Permissions > Share** and assign owner or member level permissions. 

## Customize the app icon and label in the Teams app bar

>[!NOTE]
>  For customers with at least one F license:  
> - For TAP customers, and other customers in Ring 3.6, the Viva Connections app is automatically pinned in the Teams app bar. If you don’t want the app pre-pinned, either [turn off tailored apps for frontline workers](/microsoft-365/frontline/pin-teams-apps-based-on-license), change the [app settings](/microsoftteams/teams-custom-app-policies-and-settings), or [edit how apps in Teams are managed](/microsoftteams/manage-apps).
> - For Targeted release customers (in Ring 3.6 or higher), all users at your organization will have access to the Viva Connections app. [Use audience targeting](use-audience-targeting-in-viva-connections.md) to promote specific content to different groups until the experience becomes generally available in 2023 where you’ll have access to more than one home experience option for multiple audiences.

Your organization’s Viva Connections app can display a custom icon and label in the Teams app bar. This customization takes place in the Teams admin center which requires Teams admin permissions or higher. It’s recommended that you also apply app settings that [pre-pin and pre-install the app](/microsoftteams/teams-app-setup-policies) to make sure people in your organization can more easily discover it and get immediate use. Learn more about [customizing the Viva Connections icon, label, and app settings](add-viva-connections-app.md). 

## Customize the banner image

Change the banner image in the header and set the focal point for the image. The banner image only displays in the desktop app.

1.	Start by selecting Edit and then select Change image.
2.	Select the image you’d like to use and then select Reposition. 
3.	Once you are satisfied with the focal point, select Set focal point and then Save. There is no draft state for the banner image. It will be displayed for all users when you select Save.

>[!NOTE]
> - The greeting is automatically generated and cannot be customed.
> - Depending on your organization’s license type, you may see additional dynamic information displayed in the banner.
> - The Microsoft Viva icons and labels displayed below the greeting are automatically displayed based on the license that’s detected and cannot be customed. 

## Customize the Dashboard

The [Viva Connections Dashboard](/create-dashboard.md#overview-of-how-to-create-a-dashboard-and-add-cards) provides fast and easy access to information and job-related tasks. Add and edit cards that help users quickly access the tools and resources they use in their day-to-day role. Cards on the Dashboard can be targeted to users based on specific roles, regions, and interests. Edits (including audience targeting settings) made to cards on the Dashboard will also automatically be applied to the [Dashboard web part](use-dashboard-web-part-on-home-site.md) and [the mobile experience](/viva-connections-overview.md#the-viva-connections-mobile-experience). 

>[!NOTE]
> - If your organization already has Viva Connections set up, you’ll see your existing cards and settings displayed in the new home experience. 
> - If your organization doesn’t already have Viva Connections set up, you’ll see a set of default cards that need minimal configuration.  

### Summary of default Dashboard cards and how to set them up

By default, cards will already be on the Dashboard and require minimal set up. Edit and preview the Dashboard until you are ready to share with others. 

To edit existing cards, select the pencil icon to **Edit** the card. In the property pane that opens on the right, choose your card size from the **Card size** drop-down list. 

Apply **Audience targeting** so this card is filtered to specific roles, regions, or departments. Learn more about [audience targeting for Viva Connections](use-audience-targeting-in-viva-connections.md).

| Dashboard cards | How to use the card | Default card by license type | 
| :------------------------| :-------------------| :----------------------|
| [Approvals](create-dashboard.md#add-the-approvals-card) | Request time off, approve expense reports, and sign-off on documents.  | Frontline worker SKU        |
| [Assigned tasks](/create-dashboard.md#add-the-assigned-tasks-card)  | Review and complete daily tasks assigned by your manager or team. | Frontline worker and Enterprise SKU        |
| [Shifts](/create-dashboard.md#add-a-shifts-card) | Clock-in and clock-out of shifts and view upcoming shifts and breaktimes. | Frontline worker SKU        |
| [Top news](/create-dashboard.md#add-the-top-news-card) | View the most important news from inside your organization. Use [News boost](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83) get news posts from organizational news sites to display in this card.  | Frontline worker and Enterprise SKU           | 
| [Viva Learning](/create-dashboard.md#add-a-viva-learning-card) | View recommended and required training courses. | Enterprise SKU           | 
| Viva Topics    | Share and contribute to your organization’s knowledge base. | Enterprise SKU           | 

### Preview the Dashboard before sharing with others

After creating or editing cards on the Dashboard, make sure you preview the experience for each audience and on both desktop and mobile devices by selecting Preview in the top-right corner of the editing experience. What you see in preview mode approximates how the Dashboard will display for certain audiences and devices. When you apply audience targeting to cards, you can preview how different people will view the Dashboard depending on the audience or device.

## Customize Resources

Resources gives access to the most popular portals and destinations at your organization. The Resources section displays at the bottom of the home experience and can also be accessed by selecting the app’s icon in the Teams app bar from the landing experience. Links in Resources can be [targeted to specific audiences](use-audience-targeting-in-viva-connections.md#apply-audience-targeting-to-links-in-resources). Edits made to the Resources section also impact [the mobile experience](viva-connections-overview.md#the-viva-connections-mobile-experience) and [SharePoint global navigation](sharepoint-app-bar.md) when it’s enabled. 

>[!NOTE]
> Content in Frequent and Followed sites are dynamically displayed based on the viewers interests and activity and cannot be edited. 

**If you have a home site:**
If you have already set up navigational links in the [SharePoint global navigation](sharepoint-app-bar.md), you’ll see the same content in Resources. When edits are made in Resources from Viva Connections in Teams, the same labels and links in global navigation will be edited at the same time. 

**If you do not have a home site:**
Editing Resources in the Viva Connections desktop experience will not have an impact in SharePoint or any other M365 experience. 

### To edit Resources:

1.	Start by selecting **Edit**.
2.	Hover over the Resources panel until you see a **+** (plus) icon. Select it, and then choose to add a **Link** or **Label**. Labels do not link to other destinations. 
3.	To add a new link, select **Link** from the drop-down menu paste the URL to the site in the Link field. Only modern SharePoint sites and certain Microsoft 365 experiences will display in Teams. All other types of content will open in a separate browser window. 
4.	To add a new label, select **Label** from the drop-down menu and type a label in the Label field.
5.	Audience targeting can be applied to each label and link if desired by entering groups into the field. Add up to 10 [azure Active Directory groups](/microsoft-365/community/all-about-groups) (including security groups, Microsoft 365 groups, and AAD dynamic groups). 
6.	Select **Save** to share with others. 

## Learn more about how to influence content in the Feed

There’s no configuration required to get the Feed working in the desktop or mobile apps. Content in the Feed can’t be edited because content is aggregated from across your M365 environment. Content comes from three primary sources: organizational news published in SharePoint, posts in Yammer communities, and videos in Stream that are shared with the entire organization or targeted to user groups.

The [Feed web part for Viva Connections](use-feed-web-part-for-viva-connections.md) displays the same content and can be added to other SharePoint sites. Content that is displayed in the Feed can’t be edited but the ranking can be influenced with the following actions: 
- **Promote important ‘official’ communications** - Use [News boost](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83) to raise the visibility of crucial news posts from organizational news sites.
- **Highlight community discussions** - Feature posts in public Yammer communities that you’d like seen by the entire organization.
- **Publish from official news sources** - Like [organizational news sites](/sharepoint/organization-news-site) or [home sites](/sharepoint/home-site). Where content is from impacts the ranking.
- Learn more about [how content in the Feed is sourced and ranked](faqs-viva-connections-feed.md).

## Manage permissions

The permissions model for the new Viva Connections landing experience is similar to the permissions in SharePoint. Certain levels of permission will grant access to specific editing tools and the ability to manage permissions and sharing. 

>[!NOTE]
> At least two people should be assigned to Owner level permissions. 

| Owner       | Member            | Visitor     |
|:------------------- |: -------------------|:---------------|
| Can edit content in the banner, Dashboard, and Resources. <br><br> Can add or remove owners, members, and visitors.| Can edit content in the banner, Dashboard, and Resources.  | Visitors are the end users in your organization. <br><br> They can view and interact with content but can’t edit content or share the page with others. |

If you already have Viva Connections setup, editors who have site owner or member permissions to the home site will automatically have owner or member permissions to edit the new home experience in Teams. 

   - People with member permissions *or higher* will automatically see **Edit** buttons in the home experience.
   - People with member permissions or higher will be able to view permissions to the page by navigating to the ellipsis menu in the top-right and selecting **Manage permissions**.

If you are setting it up *for the first time*, only the SharePoint root site owners will be able to edit the home experience in Teams. When the home experience is edited for the first time, a SharePoint site on the backend will get created. You’ll want to assign owners and members from this site to give permissions to others so they can edit the experience for the rest of the organization. Manage permissions from the backend site by going to **Settings > Permissions > Share** and assign owner or member level permissions. Once permission levels are assigned, people with owner or member permissions will automatically see **Edit** buttons in the home experience.

### How to add, view, and edit permissions

If you have member permissions or higher you can view who has permission to view and edit the home experience. Access permissions by navigating to the ellipsis menu (**...**) in the top-right corner and then select **Manage permissions**.

If you have owner permissions or higher, you can give access to new people and change the roles of the people who already have access. Select **Share** to give access to new people. Edit the roles of existing people by selecting the drop-down arrow and then select a new role. Changes will be applied immediately.

## Help end users in your organization learn more

>[!NOTE]
> For customers who already have Viva Connections setup, your end users will be automatically routed to the new home experience in Teams if your organization decides to use the new design as the default experience. If your organization has a home site, you can choose to keep it as the default home experience when the new experience is available. More details will be shared soon. 

When end users in your organization view the Viva Connections landing experience for the first time, they will have the option to see a basic walkthrough tutorial that shows them how to engage with content and navigational elements. Help end user [see what else they can do in the home experience](https://go.microsoft.com/fwlink/?linkid=2208247). 

## Learn more

[More options coming soon for the Viva Connections desktop experience](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/more-options-coming-soon-for-the-viva-connections-desktop/ba-p/3644419) 

[Overview: Viva Connections](viva-connections-overview.md)

[Use audience targeting in Viva Connections to personalize the experience](use-audience-targeting-in-viva-connections.md)

[Watch: How to add and edit cards in the Dashboard](create-dashboard.md#overview-of-how-to-create-a-dashboard-and-add-cards)
