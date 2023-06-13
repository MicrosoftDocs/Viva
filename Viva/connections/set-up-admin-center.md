---
ms.date: 05/16/2023
title: Set up Viva Connections in the Microsoft 365 admin center 
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
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
  - Tier1
ms.custom: intro-get-started
search.appverid:
- SPO160
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: "Learn how to set up Viva Connections in the Microsoft 365 admin center"
---

# Set up Viva Connections in the Microsoft 365 admin center

> [!NOTE]
>
> - This experience is rolling out to private preview customers now and will become generally available to all customers by the end of June 2023.
> - You must have an Enterprise (E) or Frontline (F) license type to create multiple Viva Connection experiences.
> - Viva Connections does not have any requirements to get started.
> - Users with a basic Microsoft 365 subscription (E license) are limited to creating 3 experiences. Users with a Microsoft Viva Suite subscription are at present limited to creating 10 experiences. See Microsoft Viva plans and pricing for more info.
> - You must have Global Admin or SharePoint admin permissions to access the Microsoft 365 admin center.
> - You must have Teams administrator (or higher) permissions to pin the Viva Connections app in the Teams Admin Center.

[Microsoft Viva Connections](viva-connections-overview.md) is an employee experience app in Microsoft Teams that brings together relevant news, conversations, resources, and tools in one place for every employee. It's built on your current Microsoft 365 ecosystem to help you engage, inform, and empower your workforce. The Viva Connections experience is deployed and accessed in Microsoft Teams.

Use these step-by-step instructions to help you set up and launch Viva Connections experiences in the Microsoft admin center (MAC) for your organization.

## Before getting started

Setting up Viva Connections only takes a few steps but there are some considerations to think through with other stakeholders at your organization before getting started:

- **Consider the type of experience(s) that are best for your organization**: You can create a stand-alone Viva Connections experience, or you can create a Connections experience that also builds off an existing intranet portal or SharePoint home site. You can create a single Connections experience for your entire organization with Dashboard cards targeted to specific audiences (i.e. Centralized HR communication), or you can create multiple experiences to meet the needs of distinct audiences (e.g. separate content for front-line workers, subsidiaries needing separate content and branding, etc.). Keep in mind that if you have multiple experiences with overlapping content, each experience will need to be updated separately. Learn more on how to plan, build, and launch Viva Connections.

- **Decide which audiences should be associated with each experience**: You can create more than one Connections experiences if your organization has a need for different employee experiences for distinct audiences. Decide which experiences should be associated with specific audiences. You’ll want to consider the order of experiences that should be seen for audiences that may belong to more than one experience.

- **Think about who should have owner permissions to each experience**: [Owners have full permissions to edit the experience](edit-viva-home.md) and manage access for others. As a best practice, it’s recommended that each experience has a minimum of two owners assigned to it.

- **Pick an icon and name for your app**: Choose an app icon and name to apply to your entire Connections experience. This icon and label will display as an app in the Teams app bar. Consider what the right branding elements are for your Connections experience. You’ll want to pick a name that aligns with your organization’s brand and target audience, and one that’s also meaningful and recognizable to viewers.

> [!NOTE]
> Currently the app icon and name can be managed only at a tenant level. Organizations with multiple experiences will not see individual names and icons for each one in Teams.

## How to access Viva Connections in the Microsoft admin center

1. Navigate to [admin.microsoft.com](https://admin.microsoft.com/Adminportal/Home#/homepage) and sign in with your credentials.
2. Select **Setup** and under featured collections, select **Microsoft Viva**.

   :::image type="content" source="../media/connections/set-up-admin-center/microsoft-viva-option.png" alt-text="Screenshot showing how to navigate to the Microsoft Viva admin center." lightbox="../media/connections/set-up-admin-center/microsoft-viva-option.png":::

3. Select **Viva Connections** to open the Viva Connections admin center.
4. The Viva Connections admin center will open. If you already have a SharePoint home site (intranet portal), Viva Connections will display it as an experience automatically.

## Create a new Viva Connections experience

Create an all-encompassing Connections experience for the entire organization, or for distinct audiences. Optionally, when you create a new experience, you can choose to create a stand-alone Connections experience, or to create a Connections experience and [build off an existing intranet portal (SharePoint home site)](/viva/connections/viva-connections-overview#how-sharepoint-home-sites-and-viva-connections-work-together).

:::image type="content" source="../media/connections/set-up-admin-center/set-up-viva-connections-as-admin.png" alt-text="Screenshot of steps to setting up Viva Connections as an admin." lightbox="../media/connections/set-up-admin-center/set-up-viva-connections-as-admin.png":::

> [!NOTE]
>
> - Organizations are limited to creating a maximum of ten Viva Connections experiences overall per tenant.
> - A Microsoft Viva Suite license is required to create more than three Viva Connections experiences. Check the [current license for your organization in billing under licenses](https://www.microsoft.com/microsoft-viva/pricing).
> - You must have Global admin permissions, SharePoint admin permissions, or higher to access the MAC.
> - If this is the first time you're setting up Viva Connections, it's recommended you pin the app in Teams.

### Step 1: Create a new experience

Admins will be able to create multiple standalone experiences well as intranet home sites having their own Viva Connections experience. As a result, there are now two options for creating a new experience:

> **A. Creating a Connections experience**: The option is the fastest way to get started. It creates a standalone, out-of-the-box Connections experience as an app in Teams without the need for an existing intranet portal. A special site container will be created where the Dashboard, resource, and overall Viva home experience is hosted and sourced from. Owners can then begin adding their own content. An intranet portal can be added at any time and designated as a home site.
<br>
<br>
> **B. Build from an existing intranet portal**: This option is ideal for organizations that already have a SharePoint communications site and would like to use their own content, or would like to add an intranet portal that includes Connections components that can easily be extended to the Web. This option creates a new Connections experience and automatically designates the communications site as a home site (intranet portal) that displays navigational elements, and shares permissions.

   :::image type="content" source="../media/connections/set-up-admin-center/create-new-viva-connections-experience.png" alt-text="Screenshot showing options for creating a Viva Connections experience." lightbox="../media/connections/set-up-admin-center/create-new-viva-connections-experience.png":::

#### Create a Connections experience

This option is ideal if your organization doesn't have an existing intranet portal and just needs to create an experience. This option provides a lightweight experience without a SharePoint intranet portal that users can use to add their own content. Once the Connections experience is created, it can be set as a SharePoint intranet portal (it can be accessed from SharePoint), or, an existing intranet portal can be added.

1. Select **+ Create new**, displayed on top of the list of experiences.

   :::image type="content" source="../media/connections/set-up-admin-center/option-to-create-new-connections-experience.png" alt-text="Screenshot of the option to create a new Connections experience highlighted." lightbox="../media/connections/set-up-admin-center/option-to-create-new-connections-experience.png":::

2. Select **Create a Connections experience**, then select **Next**.

   :::image type="content" source="../media/connections/set-up-admin-center/select-create-connections-experience.png" alt-text="Screenshot of selecting to create a Connections experience." lightbox="../media/connections/set-up-admin-center/select-create-connections-experience.png":::

3. Give the new experience a name, add a description, decide the settings, and then select **Next**.

   > [!NOTE]
   > The name given to the experience in the MAC will also display for owners and members who help manage and edit experiences.

4. After reviewing your settings, select **Create experience**.

   > [!NOTE]
   > Each experience you create won't be accessible by viewers until permissions have been assigned by the experience's owners and it’s been enabled.

#### Build from an existing intranet portal

If your organization has an existing intranet portal, then this option allows you to use the existing content, or add an intranet portal that includes Connections components that can easily be extended to the Web.

1. Select **+ Create new**, displayed on top of the list of experiences.

   :::image type="content" source="../media/connections/set-up-admin-center/option-to-create-new-connections-experience.png" alt-text="Screenshot of the option to create a new Connections experience highlighted." lightbox="../media/connections/set-up-admin-center/option-to-create-new-connections-experience.png":::

2. Select **Build from an existing intranet portal**, then select **Next**.

   :::image type="content" source="../media/connections/set-up-admin-center/build-from-existing-intranet-portal.png" alt-text="Screenshot of selecting to build a Connections experience from an existing intranet portal." lightbox="../media/connections/set-up-admin-center/build-from-existing-intranet-portal.png":::

3. Paste the URL of your SharePoint communication site in the **URL of the communication site you want to use** field.

   > [!NOTE]
   > The name given to the experience in the MAC will also display for owners and members who help manage and edit experiences.

   :::image type="content" source="../media/connections/set-up-admin-center/set-intranet-portal-pr.png" alt-text="The screenshot of this diagram presents the option to build a Connections experience from an existing intranet portal." lightbox="../media/connections/set-up-admin-center/set-intranet-portal-pr.png":::

4. After reviewing your settings, select **Create experience**.

   > [!NOTE]
   > Each experience you create won't be accessible by viewers until it’s been enabled, and permissions have been assigned by the experience's  owners.

#### Choose the landing destination in the Viva Connections app

Customers building from an existing intranet portal will be able to choose the landing destination for audiences in Teams via PowerShell command. (See Choose the default landing experience for Viva Connections desktop for more info).

PowerShell functionality will be limited initially as follows:

>
| **Command** | **Result** |
|----|----|
| **Get-SPOHomeSite** | Returns the single home site URL. <br><br> With multiple Viva Connections home sites, it will show a warning message and show the first Viva Connection home site from the list.
| **Set-SPOHomeSite** | 1. Initially it will continue supporting a single home site setup. Setting up more home sites can be done in the MAC. Support for setting up multiple home sites will be supported at a later stage. <br><br>2. It updates the Viva Connections default landing destination (Viva Connections, home site, or draft status for a home site). This functionality will continue getting support in multiple Viva Connection home sites. The cmdlet can be run with the home site URL to set the landing destination.
| **Remove-SPOHomeSite** | This won't be supported initially for multiple home sites customers, but the MAC will support this operation. Users attempting to use the cmdlet will receive an error message and be redirected to the MAC. |
>

#### When to use a separate experience vs Dashboard card level targeting

Depending on the size of your organization and the information to communicate, you may decide to create a separate experience for each audience you wish to target or use card-level targeting in your Dashboard to provide a targeted experience. There are scenarios in which you may choose one or the other. For information on these scenarios, see [Scenarios for creating additional Viva Connections experiences](#scenarios-for-creating-additional-viva-connections-experiences).

##### Scenarios for creating additional Viva Connections experiences

- Subsidiaries that need their own content.
- Not wanting employees to have to visit the experience of another subsidiary.
- International legal entities that need control over the content.
- Presenting international content in a different language that won't overlap with existing content (for example, English experience, Spanish experience, and so on).
- Content specific to frontline workers (for example, Dashboard and resources with the frontline worker focus such as tasks, shifts, approvals, and top news).

If creating multiple experiences, make sure you don't have any overlap with your content authors, content plan, or audience groups. Overlap will require you to manually manage the content across each experience.

##### Scenarios for card-level targeting and end-user personalization

- Creating a mix of corporate- and department-specific content (for example, centralized HR or corporate communications).
- Decluttering the Dashboard to prevent cards from appearing to employees who wouldn't use them frequently.

When you're using card-level targeting, consider testing your dashboard with different audience groups to ensure your audiences are seeing the content you want them to.

### Step 2: Assign permissions

Assign two or more owners to each experience so that they'll have full access to [edit the experience and manage permissions and access for others](edit-viva-home.md).

1. After creating your Connection experiences, select the experience to assign owners to it.
2. Select the **Permissions** tab from the settings panel. The owners assigned to the experience will display here.
3. Select **Add**.

   :::image type="content" source="../media/connections/set-up-admin-center/add-permissions-to-assigned-owners.png" alt-text="Screenshot of the screen on which you can add permissions to owners of experiences." lightbox="../media/connections/set-up-admin-center/add-permissions-to-assigned-owners.png":::

4. Enter the names of the people you want to assign as owners to this experience in the search bar.
5. Select **Add** after you've finished entering the names.
6. If you want to add more owners later, select **+ Add owners** under the **Permissions** tab.

   :::image type="content" source="../media/connections/set-up-admin-center/add-additional-owners.png" alt-text="Screenshot of the screen on which you can add more owners to an experience." lightbox="../media/connections/set-up-admin-center/add-additional-owners.png":::

### Step 3: Designate audiences

Decide which Azure Active Directory security groups or Microsoft 365 groups should be associated with each Viva Connections experience. Adding audiences doesn't grant permissions to the experience but creates associations to scope down who should see the experience by default. Later, owners will assign member- and visitor-level permissions to grant access to the experience, and will further filter the experiences through audience targeting.

> [!NOTE]
> Visitors are set to **Everyone in the company except external users** by default.

Audience targeting can be set up by doing either of the following tasks:

1. Assigning one or more Azure Active Directory security groups or Microsoft 365 groups to the experience (This is the most common scenario).
2. Assigning license-level filtering, and choosing if frontline workers (F-license holders) or non-frontline workers should be targeted. (This option has been introduced to account for a scenario where a targeted experience for frontline and information workers is needed.)

In this example scenario, Contoso Retail wants to target all sales frontline workers for a specific Connections experience. However, they have an Azure Active Directory (Azure AD) group for ‘Contoso Sales All’ that includes sales directors and higher who are non-frontline workers. To set up the audience targeting, the Azure AD group ‘Contoso Sales All’ license filtering option should be set to **frontline workers**. This setting will filter down the experience to only members of the ‘Contoso Sales All’ group who are also frontline workers (F-license holders). If the end user selects both options, an ‘AND’ operation is created, and the end user has to satisfy both the group and the license filtering criteria to access the experience.

Users who have already designated audiences for their experiences can use the following steps to manage their audiences:

1. After creating your Connection experiences, select the experience to assign audiences to it.
2. Select the **Audience** tab from the settings panel.
3. Select **Edit audience**.

   :::image type="content" source="../media/connections/set-up-admin-center/designate-audiences.png" alt-text="Screenshot of the screen on which you can designate audiences to experiences." lightbox="../media/connections/set-up-admin-center/designate-audiences.png":::

4. To create an experience for the entire organization, select **Everyone in the organization**.
5. To create an experience for a distinct audience, select **Scope down the audience for this experience**. Then, you can filter audiences by license type, by Azure AD/M365 group, or by both.
    1. **Add by group**: Filter based on the Azure AD/M365 group by typing the group name(s) in the search bar.
    1. **Add by license type**: Filter based on the subscriber license type.

> [!NOTE]
> If filtering by Microsoft 365 group and license options, only audiences who belong to both will be associated. For example, an administrator may want to create a distinct experience for a subset of all the frontline workers.

6. Select **Save** when you're done.

   :::image type="content" source="../media/connections/set-up-admin-center/editing-audience.png" alt-text="Screenshot of the screen on which you can save the setting of designating audiences to experiences." lightbox="../media/connections/set-up-admin-center/editing-audience.png":::

   The audiences will display here under **Groups** and can be edited in the future.

   :::image type="content" source="../media/connections/set-up-admin-center/display-of-audience-data-under-groups.png" alt-text="Screenshot of the screen displaying details of the audience under Groups tab." lightbox="../media/connections/set-up-admin-center/display-of-audience-data-under-groups.png":::

### Step 4: Decide the order

If your organization has multiple experiences, some audiences may belong to more than one. By setting an order for each experience, you can determine the priority in which experiences will be seen first. Experiences should be ordered based on the size of the targeted audiences, from the smallest to the largest. This pattern will ensure your smaller audiences will see their tailored experience without being flooded with information that larger, more general, audiences may receive.

#### Example of how ordering works with multiple experiences

:::image type="content" source="../media/connections/set-up-admin-center/how-ordering-works-with-multiple-experiences.png" alt-text="Screenshot of the screen that describes how ordering works with multiple experiences." lightbox="../media/connections/set-up-admin-center/how-ordering-works-with-multiple-experiences.png":::

In this example (in the screenshot), there are two Connections experiences for an organization. Both “Relecloud” experiences have been enabled and can be seen by viewers.

The experience named **Relecloud – FLW** is scoped to frontline workers at the organization who also belong to the “Relecloud” experience, but this experience also provides the specific information relevant to the frontline workers. The **Relecloud** experience is targeted to all employees at the organization and provides information targeted to everyone.

Since the frontline workers belong to more than one experience, the **Relecloud – FLW** experience should be ordered to come before the experience set to the **Everyone** audience. By ordering the scoped experience first, you create a rule that prioritizes displaying this experience over the default experience for users who belong to more than one experience.

If the example organization creates another experience scoped to a subset of the audience, they'll need to reorder experiences again to ensure the most scoped experiences are prioritized over the default experience.

#### To set the order of experiences

1. Select **Change order**.
2. Drag and drop the handles next to each experience to reorder as desired.
3. Select **Save** when you're done.
  
   :::image type="content" source="../media/connections/set-up-admin-center/set-order-of-experiences.png" alt-text="Screenshot of the screen on which you set the order of experiences." lightbox="../media/connections/set-up-admin-center/set-order-of-experiences.png":::

### Step 5: Enable the experience

Enable each Viva Connections experience to make it visible to your audience.

1. Select a Connection experience.
2. In the **General** tab, under **Status**, select **Edit status**.

   :::image type="content" source="../media/connections/set-up-admin-center/edit-status-option.png" alt-text="Screenshot of the screen on which you can edit the status to enable the experience." lightbox="../media/connections/set-up-admin-center/edit-status-option.png":::

3. Select the **Enable experience** checkbox, and then select **Save**.

   :::image type="content" source="../media/connections/set-up-admin-center/enabling-experience-saving-setting.png" alt-text="Screenshot of the screen on which you enable the experience and save the setting." lightbox="../media/connections/set-up-admin-center/enabling-experience-saving-setting.png":::

If you need to update the experience, you can also return it to **Draft** status and hide it from viewers.

## Pin the Viva Connections app in Teams

> [!NOTE]
>
> - The Viva Connections app only needs to be pinned to Teams once after the creation of your first experience, unless you are pinning by policy.
> - If you are pinning by a policy, revisit your pinning policy to make sure the Viva Connections app is pinned correctly for intended users every time you add a new experience. See Manage app setup policies for more info.
> - Teams administrator (or higher) permissions are required.

Viva Connections creates web parts for organizations who build off existing intranet portals, or home sites which can be accessed via Microsoft Teams. The app is auto enabled by default, but to make Viva Connections easily discoverable, it’s recommended to pin the app. Once the app is pinned, your organization’s icon and custom app name will appear in the Teams app bar.

> [!NOTE]
> Pre-pinning the Viva Connections app doesn't change the Microsoft Teams experience and doesn't automatically open the app in Teams. Pre-pinning makes it easier to discover and use the Viva Connections app.

1. Navigate to **Teams admin center > Teams apps > Setup policies**.
2. Select **Global (Org-wide default)** (this is the default policy for all users).
3. Scroll down to **Pinned apps**.
4. Select **+ Add apps**.
5. In the second box, search for the Viva Connections app you enabled with the name you gave it; for example, Intranet.
6. Select **Add** next to the app name, and then, select **Add** at the bottom of the panel.
7. Use the two horizontal lines next to the app to drag it to the top of the app list.
8. Select **Save** at the bottom of the page.

Learn more about [Adding the Viva Connections app in the Teams Admin Center](add-viva-connections-app.md).

### Options in the settings panel

The following screenshot provides an overview of the settings available in the settings panel:

:::image type="content" source="../media/connections/set-up-admin-center/settings-overview.png" alt-text="Screenshot with an overview of the settings in the settings panel." lightbox="../media/connections/set-up-admin-center/settings-overview.png":::

1. **Open in Teams**: Open this experience in the Teams app.
2. **Analytics**: Download data for overall traffic, usage, and usage by platform for the selected experience in an Excel spreadsheet (Learn more about [Usage data for Viva Connections](viva-connections-analytics.md)).
3. **Delete**: Permanently delete the selected Viva Connections experience.
4. **General tab**: Provides settings to manage the selected experience.
5. **Audience tab**: Create audiences to associate with the selected experience.
6. **Permissions tab**: Assign owners who have permission to edit content in the selected experience.
7. **Experience name**: Edit the name of the selected experience (visible only to administrators in the MAC).
8. **Status**: Indicates if the status of the selected experience is **Draft** or **Enabled**.
9. **Experience description**: A brief description of the experience for administrators (not commonly seen by users).
10. **URL**: Location of the intranet home site (if one has been added) or the special site container (if the experience wasn't created from an existing intranet portal).
11. **License type**:  Which license type the experience has been scoped for (for example, frontline workers, enterprise, or all).
12. **Creation date and details**: Information on the creation of the experience.
13. **Time zone**: What time zone the experience is set for.
14. **Default language**: What default language the experience is set as.

### Delete a Connections experience

> [!IMPORTANT]
> 
> Deleting a Viva Connections experience will remove it from your list of experiences. However the site will still remain available under the list of active sites in the SharePoint Admin Center (SPAC).
>
> - If the experience was tied to an intranet portal-based experience, the home site designation will be removed and the site will become a regular SharePoint communication site again.
> - If the experience was a standalone Connections experience, it will be removed from the list but the special site container, and the content, will still be available through the active sites in SPAC.
>
> It is encouraged to move expired or ‘out of service’ experiences to a draft state to keep the experience intact.  

1. Select the experience you wish to delete.
2. In the settings panel, select **Delete**.

   :::image type="content" source="../media/connections/set-up-admin-center/deleting-experience.png" alt-text="Screenshot of the screen on which you can delete a Viva Connections experience." lightbox="../media/connections/set-up-admin-center/deleting-experience.png":::

3. A confirmation screen will display. Select **Delete** to remove the experience.

   :::image type="content" source="../media/connections/set-up-admin-center/completing-deletion-of-experience.png" alt-text="Screenshot of the screen on which you can click the final option to complete deletion of a Viva Connections experience." lightbox="../media/connections/set-up-admin-center/completing-deletion-of-experience.png":::

### Add a SharePoint home site after setting up a Connections experience

  :::image type="content" source="../media/connections/set-up-admin-center/setting-home-site-after-setting-up-connections-experience.png" alt-text="Screenshot showing an example of a SharePoint home site after set up." lightbox="../media/connections/set-up-admin-center/setting-home-site-after-setting-up-connections-experience.png":::

> [!IMPORTANT]
>
> - Organizations that are not Viva Suite subscribers are limited to creating three Viva Connections experiences.
> - Viva Suite subscribers are limited to creating a maximum of ten Viva Connections experiences.

Connections and home sites (also referred to as intranet portals) are two complementary methods to creating powerful employee experiences that can be viewed on the web and in Teams. [Learn more about how Connections and homes sites work together](/viva/connections/viva-connections-overview#how-sharepoint-home-sites-and-viva-connections-work-together).

A home site is not required to set up Viva Connections, but it’s recommended that you add one while setting up Connections to reduce the risk of needing to manually copy content between experiences in some cases. [Learn more about how to plan and build a home site](/viva/connections/home-site-plan).

Take the following scenario:  An organization that does not have an existing intranet home site creates a Viva Connections experience using the standalone out-of-the-box option during creation. Over a year the organization populates the experience with content.

A year later, the organization begins to develop a SharePoint communication site for their content and wants to set the SharePoint home site with a Viva Connections experience so their employees can access the content on SharePoint as well as in the Viva Connections app in  Teams.

The organization would need to create a new experience, this time building their experience from an existing intranet portal (i.e. the SharePoint communication site). Once the new experience has been fully set up (e.g. permissions assigned, audiences designated, order), the content from the initial standalone experience will need to be recreated in the new experience built from the intranet home site. Once the content from the old experience has been manually recreated over to the new experience, admins would need to put the old experience into a draft status or delete it and enable the new experience. This would direct visitors to the new experience where they can access the content from the Viva Connections app in Teams or SharePoint.

#### To add a home site after you've set up a Connections experience

1. Follow the steps outlined for [building from an existing intranet portal](#build-from-an-existing-intranet-portal).
2. If your organization has already set up content in the Connections dashboard and the navigation sections from Teams, you’ll need to manually copy content to the home site in SharePoint, otherwise the original content will be hidden in Teams when you publish the home site.

If your organization doesn’t have any custom Connections content in Teams yet, you do not need to manually copy content. Instead, you can **Save** the home site and enable the experience.

   :::image type="content" source="../media/connections/set-up-admin-center/copy-content-to-home-site.png" alt-text="Screenshot showing an example of a SharePoint home site." lightbox="../media/connections/set-up-admin-center/copy-content-to-home-site.png":::

3. For organizations who have already set up dashboard and navigation content in Teams, keep the home site in **Draft mode** until the content has been copied to the home site in SharePoint.

#### How to copy content to the home site in SharePoint

Follow these instructions if your organization already has custom Connections dashboard and navigation content set up from Teams that you want to preserve when you add a home site.

> [!NOTE]
> You'll need SharePoint admin permissions or higher to complete the following steps.

1. Keep the new home site in **Draft mode** until content has been copied to the home site in SharePoint.

  :::image type="content" source="../media/connections/set-up-admin-center/sharepoint-settings.png" alt-text="Screenshot showing the setting options in SharePoint." lightbox="../media/connections/set-up-admin-center/sharepoint-settings.png":::

2. Navigate to SharePoint and go to the home site. Next go to **Settings**.
3. Copy dashboard content from Teams to SharePoint. To set up the dashboard from the home site, go to **Set up Viva Connections > Create dashboard**. Preview and then **Publish** the dashboard when it’s ready to be shared with others.
4. Copy content in the navigation column in the Resources section to global navigation in SharePoint. Go to **Global navigation > Enable** and then customize the navigational links. These links will automatically populate the navigation column in the Resources section of the Connections experience.
5. After all the content you want to preserve has been copied to the home site in SharePoint, navigate back to the Connections experience in the MAC and turn the **Draft mode** toggle off and then select **Save**.

## Related Articles

- [Overview: Viva Connections](viva-connections-overview.md)
- [Microsoft Viva Adoption](https://adoption.microsoft.com/viva/)
- [Overview of Viva Connections Extensibility](/sharepoint/dev/spfx/viva/overview-viva-connections)
- [Customize and edit the Viva Connections home experience](edit-viva-home.md)
