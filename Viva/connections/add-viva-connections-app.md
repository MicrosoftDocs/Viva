---
ms.date: 03/20/2023
title: Add the Viva Connections app in the Teams admin center
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
description: "Learn how to add the Viva Connections app in Microsoft Teams"
---

# Add the Viva Connections app in the Teams Admin Center

After you have [prepared your intranet for Viva Connections](viva-connections-setup-guide.md) in SharePoint, you are ready to add the Viva Connections app in the Microsoft Teams Admin Center. Add the Viva Connections app, and then customize app settings to add your organization's logo, pre-install, and pre-pin the app for end users. 

> [!IMPORTANT] 
> - Teams administrator (or higher) permissions are required to add the Viva Connections app to the Teams Admin Center.


![Image of Viva Connections app in the Teams admin center.](../media/connections/viva-teams-add-app.png)


## Start by adding the app in the Teams Admin Center

1.	Log in to the Microsoft Teams admin center
2.	Select **Teams Apps** and then **Manage Apps**
3.	Search for “Viva Connections”, and select the **Viva Connections app**

> [!NOTE]
> The Viva Connections app is blocked by default.


## Next, customize the app

![Image of the app customization panel.](../media/connections/viva-app-customize.png)

1. Select **Actions** in the top-right area and then select **Customize**

2. From the **Customize** panel, update the attributes under details. 

   The **Short name** will be the display name of the Viva Connections app in your tenant.  In this example, it is “Relecloud”. 

   ![Image of the app customization panel for the app logo.](../media/connections/viva-app-customize-logo.png)

3. Next, select **Icon** at the bottom of the **Customize** panel.

4.  Upload a full color icon 192x192px and also upload a transparent outline icon 32x32px. Optionally, select an accent color that will be applied on card elements in the app on Teams mobile.
 
5. Select **Apply** when you are done.



## Then, customize the app settings

Most organizations want to pin the Viva Connections app to the top of the Teams app bar for all users. This can be accomplished by changing the pinned apps in the Microsoft Teams admin center under [Setup policies](/MicrosoftTeams/teams-app-setup-policies).

> [!NOTE]
> Pre-pinning the Viva Connections app doesn't change the Microsoft Teams experience and doesn't automatically open the app in Teams. Pre-pinning makes it easier to discover and use the Viva Connections app. 

1. Navigate to the **Teams admin center** > **Teams apps** > **Setup policies**.
2. Select **Global (Org-wide default)** (this is the default policy for all users).
3. Scroll down to **Pinned apps**.
4. Select **+ Add apps**.
5. In the second box, search for the Viva Connections app you enabled with the name you gave it, for example, Intranet.
6. Select **Add** next to the app name and then **Add** at the bottom of the panel.
7. Use the two horizontal lines next to the app to drag it to the top of the app list.
8. Select **Save** at the bottom of the page.

If your needs are different, [learn more about Teams app setup policies](/MicrosoftTeams/teams-app-setup-policies).

Optionally (but highly recommended) set app permissions policies to determine which users have access to the app. [Learn more about Teams permission policies](/microsoftteams/teams-app-permission-policies).

## Finally, make the app available to end users

![Image of the app panel.](../media/connections/viva-allow-app.png)

1. Return to the Teams admin center and select **Teams apps** then **Manage apps** and search for the Viva Connections app using the name you selected as the **Short name** when you first customized the Viva Connections app.

2. Change the app from the default **Blocked by Publisher** state to the **Allowed** state.



## More resources

[Overview of Viva Connections](viva-connections-overview.md)
<br>

[Set up and launch Viva Connections](viva-connections-setup-guide.md)

