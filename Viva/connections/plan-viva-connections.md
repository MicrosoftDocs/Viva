---
ms.date: 09/22/2023
title: "Plan Viva Connections for your organization"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Plan Microsoft Viva Connections for your organization"
---

# Plan Microsoft Viva Connections for your organization

> [!NOTE]
>
> - You must have an Enterprise (E), Frontline (F), or Academic (A) license type to create a Viva Connections experience.
> - Users with a Microsoft 365 subscription (E, F, or A license) are limited to creating and using one experience. If you want to create or use two or more experiences (up to 50), then every user in your tenant must have a Microsoft Viva Suite or Viva Communications and Communities license. See [Microsoft Viva plans and pricing]( https://www.microsoft.com/microsoft-viva/pricing) for more info.
> - Viva Connections does not have any requirements to get started.
> - You must have SharePoint admin permissions to access the Microsoft 365 admin center.
> Viva Connections is available on mobile and tablet devices in GCC, GCC High, and DoD environments with limited features. Please refer to the [list of service availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#service-availability-for-each-plan) for more information.

In this phase, build a team of stakeholders to align on the goals and primary use cases for your organization's employee experience strategy. Start by meeting requirements, and then planning for each component of the experience. In the planning phase, consider success metrics and adoption tactics to ensure Viva Connections meets the need of your organization and users.

Tasks below marked with an asterisk (*) are optional, or may only apply to customers who will use SharePoint home sites to complement the Viva Connections experience.

## Step 1: Plan for Viva Connections

Viva Connections is designed to help users complete high-priority tasks and access important information. This experience can be built on overtime as your organization adapts and scales. Organizations can use their existing SharePoint intranet home site if they have one, or create a standalone experience accessible in Microsoft Teams.

Viva Connections is composed of three main parts – the dashboard, the feed, and resources. These parts will display differently on desktop and mobile devices. [Learn more about the differences between the desktop and mobile experience](/viva/connections/viva-connections-overview#viva-connections-mobile-and-desktop-experiences).

- **Dashboard:** The dashboard is your employee’s digital toolset. It brings together the tools your employees need, enabling quick and easy access whether they are in the office or in the field.
- **Feed:** The Feed delivers updates to the right people at the right time and is tightly integrated with Viva Engage, SharePoint news, and Stream to display a personalized feed, based on post-level targeting of the groups that employees belong to.
- **Resources:** The Resources experience enables way finding across platforms. It uses navigation elements from the SharePoint app bar, which can be [audience targeted](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293).

> [!NOTE]
>
> Starting **September 1, 2024**, the feed for Viva Connection web part and the video news link will be removed and unavailable for SharePoint site editors to add to their sites. On **November 5, 2024**, support for the feed for Viva Connections web part and video news links will end and no longer display content.
>
> Site owners are encouraged to use the [News](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews), [Viva Engage](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights), [File and Media](/stream/streamnew/portals-single-video), and [Highlighted content](/stream/streamnew/portals-set-of-videos) web parts, and [Video pages](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a) as alternatives to using the feed for Viva Connections web part and the video news link. For more information, refer to the [Viva Connections Feed web part retirement support guidance documentation](feed-web-part-video-news-link-retirement.md).

>
| Desktop              | Mobile              |
| :------------------- |:------------------- |
| ![Image of the Viva Connections landing experience in the desktop app.](../media/connections/vc-full-small.png)|![Image of the Viva Connections landing experience in the mobile app.](../media/connections/mobile-dashboard-small.png)|
|- Your organization’s instance of Viva Connections [will appear as an icon](/viva/connections/add-viva-connections-app#then-customize-the-app-settings) in the Teams app bar. <br> - When the icon is selected, users will see the default landing experience. <br> - When the icon is selected twice, the global navigation panel will display. <br> - Add the [Feed web part](use-feed-web-part-for-viva-connections.md) to highlight personalized news. <br> - Add the [Dashboard web part](use-dashboard-web-part-on-home-site.md) to make it easy to complete tasks | - Your organization’s instance of Viva Connections will appear as an icon in the Teams mobile app bar. <br> - Once selected, users can pivot from the dashboard to the feed to resources.|
>

## Step 2: Consider using a SharePoint home site to complement the experience* (optional)

A Viva Connections experience doesn’t require a [SharePoint home site](home-site-plan.md) (a communication site that has special capabilities) to be created, but providing one can complement the employee experience. A SharePoint home site acts as the front door to your organization’s intranet and a gateway to other popular portals that are relevant to the entire organization. [Some organizations will use a SharePoint home site to complement the Viva Connections experience](/viva/connections/viva-connections-overview#how-sharepoint-home-sites-and-viva-connections-work-together) and extend the experience to the web. Follow the steps below if your organization wants to use a SharePoint home site in addition to Viva Connections. A SharePoint home site can be added at any time.

>
| Requirement    | Description                 |
| :------------------- | :------------------- |
| Create a SharePoint home site* (optional)  | A [SharePoint home site](/sharepoint/home-site-plan) is a SharePoint communication site that acts as the front door to your organization’s intranet. They have extra capabilities such as the ability to prioritize news posted from the SharePoint home site across the rest of the intranet. Once a SharePoint home site is set, the news posted from that site will be prioritized across the intranet. SharePoint home sites are set in the Microsoft Admin Center when you create a new Viva Connections experience. To add a SharePoint home site, choose the option to build off an existing intranet portal. <br><br> Learn more about how to think about [planning navigation on your SharePoint home site](https://techcommunity.microsoft.com/t5/microsoft-sharepoint-blog/best-practices-for-using-global-navigation-in-the-sharepoint-app/ba-p/2361916) in combination with hub and global navigation. Then, get started [creating a SharePoint home site](/sharepoint/home-site-plan). |
| Set up global navigation* (SharePoint home site users only) |Once your SharePoint home site is set up, you can enable and customize global navigation in the SharePoint app bar. In the Viva Connections desktop app, resources in the global navigation panel will display when the Viva Connections icon is selected in Teams and in the resources section. In the Viva Connections mobile app, resources in the global navigation will display in the “Resources” tab. <br><br> Learn more about how to [enable and customize global navigation](/sharepoint/sharepoint-app-bar). |
| Audit, prioritize, and modernize sites* (optional) | After you've identified the key scenarios for Viva Connections, you’ll need to identify content or sites that should be modernized if you're still using classic sites and pages. Not all content or classic SharePoint sites need to be modernized to take advantage of Viva Connections. Focus on the priority use cases that will need to be included in your organization’s instance of Viva Connections. <br><br> Learn more about [how to modernize content](/sharepoint/dev/transform/modernize-classic-sites#:~:text=Modernize%20your%20classic%20SharePoint%20sites%201%20Enable%20your,site%20transformation%20is%20transforming%20your%20site%20pages.%20) and [healthy portal guidance for high-traffic sites](/sharepoint/portal-health)|
>

### Create a SharePoint home site for your organization* (optional)

A SharePoint home site is the front door to your organization’s intranet and a gateway to other popular portals that are relevant to the entire organization. Your SharePoint home site will also be the landing experience for Viva Connections in the Microsoft Teams desktop app.

   ![Image of Viva Connections desktop.](../media/connections/viva-connections-desktop.png)

Start small by identifying a handful of resources and functions that the SharePoint home site can serve. Consider using a [customizable site template from the SharePoint look book called The Landing](https://adoption.microsoft.com/sharepoint-look-book/) to quickly get your SharePoint home site up and running. Optionally, turn your SharePoint home site into a [SharePoint hub site](/sharepoint/planning-hub-sites) to add an extra layer of navigation and increase the search scope.

Learn more about [how to plan your SharePoint home site](/sharepoint/home-site-plan) and [how to launch healthy SharePoint sites](/sharepoint/portal-health).

### Set up global navigation in the SharePoint app bar* (optional)

Next, from the SharePoint home site Settings icon, select [Set up global navigation](/SharePoint/sharepoint-app-bar) to take advantage of full Viva Connections functionality. Design global navigation in a way that compliments and expands resources on the SharePoint home site. [Learn more about navigation and information architecture in SharePoint](/sharepoint/information-architecture-modern-experience).

   ![Animation of the global app bar in SharePoint.](../media/connections/app-bar-gif.GIF)

Navigational links that appear in the global navigation pane in the SharePoint app bar will also display in the Viva Connections app in Microsoft Teams for desktop and mobile apps.

### Audit, prioritize, and modernize content to align with key scenarios and tasks* (optional)

After defining the key scenarios and tasks in the planning phase, prepare for Viva Connections by ensuring priority content is located on modern SharePoint communication sites and team sites. Both modern and classic sites can be used, but only modern sites will appear in the Microsoft Teams app. Classic sites will open in a separate browser window.

If you have many classic SharePoint sites make sure you focus on sites, pages, and content that are relevant to the Viva Connections experience. Sites and content that are unrelated to key tasks and scenarios can be modernized later.

**Sites that should be audited and prioritized:**

- Sites that connect to cards on the Viva Connections dashboard
- Sites that are displayed in global navigation
- Sites that frequently publish organizational news
- Sites that help employees complete the most important day-to-day tasks or access important information

**Tools to help you modernize:**

- Use the [SharePoint modernization scanner](/sharepoint/dev/transform/modernize-scanner) to create a dashboard that helps you determine modernization readiness.
- Learn more about how to [transform classic sites to modern sites](/sharepoint/dev/transform/modernize-userinterface-site-pages), or consider [creating new modern sites using SharePoint site templates](https://support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398).
- For popular sites that are expected to get a high amount of traffic (1000s of views per day or more) [learn more about best practices for high-performing sites and portals](/sharepoint/portal-health).

## Step 3: Plan the dashboard

Start by identifying the key scenarios that Viva Connections needs to support and identify owners of those employee experiences. Tasks and scenarios will be primarily supported by cards in the Viva Connections dashboard that can be targeted to specific audiences using Microsoft 365 groups. Consider which groups of employees will need access to specific resources.

>
|Dashboard on mobile | Description |
|----- |-----|
|![Interaction between the Dashboard and cards.](../media/connections/new-vc-dashboard-interaction.gif) | In this example, a card on the dashboard is linked to a SharePoint page where users can take a daily health check easily from a mobile device.|
>
Common scenarios include view paystubs and vacation hours, submit help tickets, catch up on news, check daily lunch menus, find people in a directory, and shift management. Collaborate and align with business groups that manage these experiences to determine the best design. Review the [Adoption center's best practices from successful Viva Connections customers](https://adoption.microsoft.com/files/viva/connections/Adoption-Recommended-Practices-for-Viva-Connections.pdf) for more information on common scenarios and how to identify employee experiences that result in lasting adoption.

>
| General | For information workers   | For frontline workers  |
| :------------------- | :------------------- |:-------------------|
| - View pay and benefits <br> - Submit a ticket to the help desk <br> - Access lunch and café options <br> - Catch up on news and announcements | - Find people and team information <br> - Complete required training <br> - View company holidays | - View and manage shifts <br> - Access time sheets and popular forms <br> - View workplace policies and resources |
>

### Types of dashboard cards

As you plan, consider the different types of cards available. There are three different types of cards that can be used on the Viva Connections dashboard. Some cards may take longer than other to implement or may require work on the backend to set up.

- **Out of the box cards:** These cards require little configuring and include the [Link, Shifts, Teams, and Assigned tasks cards](/viva/connections/create-dashboard).
- **Adaptive extension cards:** Also known as ACEs, are [cards that can be extended and customized](/sharepoint/dev/spfx/viva/get-started/build-first-sharepoint-adaptive-card-extension) using the SharePoint Framework (SPFx).  
- **Third-party cards:** These cards come from [third parties like Qualtrics, ServiceNow, and Workday](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/viva-connections-welcomes-new-partners-and-opens-developer/ba-p/2540643).

### Planning process

   ![Image of a planning process flow.](../media/connections/plan-process-2.png)

As you work with business owners and key stakeholders to align your Viva Connections design strategy, answer the following for each task:

- Who is the audience?
- What do users need to accomplish or learn?
- What tools or technology do they use today?
- What tools or technology do you want visitors to use to accomplish their key tasks?
- What information needs to be promoted?

#### Start with the most important workflows

Not *every* task should be turned into a card on the Dashboard. Focus on the most impactful tasks that can be executed within a short amount of time. Find opportunities that align with the fields "Quick wins" and "First successes" in the decision matrix below as a start.  

   ![Image of a planning matrix.](../media/connections/plan-matrix.png)

#### Design with your audience in mind

As a best practice, it's important to make decisions that are rooted in specific tasks for certain audiences:

- Consider using a common framework for scenario planning that starts by selecting a certain role or audience *"As an..."*.
- Then, narrow down the objective in *"I need to..."*.
- Next, consider the ideal tool or process to meet the objective in *"So that I..."*.
- Lastly, script out what success looks like in *"I know this is successful when..."*.

For example, create a table like the following to list business scenarios that you want to address with cards in the dashboard:

>
|In my role as...|I need to...|So that...|I know this is successful when...|
|:-------------------|:---------------|:-----------|:------------------------------------|
|Full time employee |Easy access to benefit and payroll information |I can quickly check important information without needing help from HR |Requests for help with benefits and payroll to the HR team are reduced  |
|Frontline worker |Clock in and out from a mobile device |I can create efficiencies in my workflow |Schedules and breaks are managed from Viva Connections |
|People manager |Welcome and onboard new team members |I can grow and develop talent |I spend less time managing standard onboarding functions |
|Sales representative| Access specific product training materials while on a mobile device |Can quickly resolve customer issues|Most customer issues get resolved in real-time|
|HR specialist |Promote the use of the self-service benefits |I can spend more time working with employees on unique benefits questions and scenarios|All of my employee interactions are about individual critical scenarios|
>

#### Examples of different dashboard designs

The dashboard should focus on the most important tasks. Tasks that are specific to certain audiences should be targeted to make sure users only see cards that are relevant to their day-to-day jobs.

>
| Information workers   | Frontline workers  |
|-----------------------|--------------------|
| ![Image of the Viva Connections dashboard designed for frontline workers.](../media/connections/dashboard-information-worker.png) |  ![Image of the Viva Connections dashboard designed for information workers.](../media/connections/dashboard-frontline.png) |
>
#### Content for planning Dashboards

- [Create and customize a dashboard](/viva/connections/create-dashboard)
- Learn more about [adaptive cards](https://adaptivecards.io/)and  [third-party cards](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/viva-connections-welcomes-new-partners-and-opens-developer/ba-p/2540643)
- Use existing [Microsoft 365 groups](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) or create news groups if needed so that you can quickly create cards and [target them to specific audiences](/viva/connections/create-dashboard#apply-audience-targeting-to-cards)

## Step 4: Get ready for the feed

The feed brings communications from across the organization into one place where it can be easily viewed. This feed helps keep frontline workers, information workers, and hybrid workers alike engaged and informed on important news and announcements. This solution also gives content publishers a reliable method of distributing important news and information.

Technically, you do not need to do anything to set up the feed because content will sync automatically. However, you can influence the content hierarchy.

![Image of the feed in the mobile app.](../media/connections/mobile-feed.png)

### Tips on how to influence content hierarchy in the feed

The feed is designed to be dynamic, personalized, and a place where the most relevant news and announcements can be consumed. The feed relies on a constant flow of new content and the best experience contains a balance of organizational news, organic content, and curated content.

- Publish SharePoint news from [official organizational news sources](/sharepoint/organization-news-site#:~:text=Use%20Microsoft%20PowerShell%20to%20specify%20a%20site%20as,organization%20news%20site%3A%20PowerShell%20Set-SPOOrgNewsSite%20-OrgNewsSiteUrl%20%3Csite%20URL%3E) like the [SharePoint home site](/viva/connections/home-site-plan)
- [Use news boost to elevate the most important news](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83#:~:text=1%20On%20your%20organization%20news%20site%2C%20open%20the,post%20to%20stop%20being%20boosted.%20More%20items...%20) posts on organizational news sites to surface news posts to the top of the feed
- [Post news as a video news links](/viva/connections/video-news-links) hosted by stream to share updates, rebroadcast an all-hands meeting, or provide reusable training materials
- Highlight community discussions by [featuring posts in Viva Engage](/viva/engage/manage-viva-engage-groups/all-company-community) that you’d like seen by the entire organization
- Encourage your organization to [engage and participate in discussions in Viva Engage](https://adoption.microsoft.com/viva/engage), especially leaders and workplace champions
- [Use audience targeting](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293) to make sure specific content is seen by different audiences using Microsoft 365 groups

#### Content for planning feeds

- Review [frequently asked questions about the feed](/viva/connections/faqs-viva-connections-feed) for Viva Connections
- Consider using the [Feed web part](https://support.microsoft.com/office/use-the-feed-web-part-for-viva-connections-001fbe90-3778-4801-9ea9-71308711d330#:~:text=%20Add%20the%20Viva%20Connections%20Feed%20web%20part,for%20Viva%20Connections%20Feed%20web%20part.%20More%20) on popular SharePoint pages to surface news and announcements
- Learn more about [best practices for higher feed engagement](https://adoption.microsoft.com/files/viva/connections/Adoption-Recommended-Practices-for-Viva-Connections.pdf)

## Step 5: Plan the resources

Resources are the navigational links to portals and other popular destination. Resources should be the most important and popular portals for your target audience and can be targeted to specific audiences. While preparing your Viva Connections, know that these resources will display from the SharePoint app bar (if your organization has a SharePoint home site) and in the Teams app bar when Viva Connections is set up.

>
| Desktop             | Mobile                 |
| ------------------ | ------------------ |
| ![Image of global navigation in the desktop app.](../media/connections/vc-resources-new-small.png)| ![Image of global navigation in the mobile apps.](../media/connections/mobile-resources-small.png)|
>
For organizations with SharePoint home sites, consider how links in the global navigation will complement resources highlighted on the SharePoint home site. Depending on the content you want to make available in the global navigation, you can [design your SharePoint home site navigation and global navigation in three different ways](/viva/connections/sharepoint-app-bar#see-all-the-different-ways-you-can-set-up-global-navigation).

### Content for planning Resources

- Set up for the first time, or [customize navigational links in the global navigation](/viva/connections/sharepoint-app-bar) from the SharePoint home site
- Get more guidance on how to [design navigation in SharePoint](/sharepoint/information-architecture-modern-experience)

## Step 6: Create an adoption plan

Planning for change and helping users adopt new resources will be different for every organization. Use the considerations and best practices here as a starting point to creating an adoption plan that fits your organization’s needs. Include considerations for change management and training materials for end-users in your plan.

### Adoption considerations

- Viva Connections can only be accessed in Microsoft Teams. If your organization isn't already using Microsoft Teams, you'll need to [plan the adoption of Microsoft Teams](https://adoption.microsoft.com/microsoft-teams/) alongside [Viva Connections](https://adoption.microsoft.com/viva/).
- Make adoption easy for end-users by [pre-pinning the app in Teams](/viva/connections/add-viva-connections-app#then-customize-the-app-settings) while picking settings. This only needs to be done once (Viva Connections is auto-enabled by default in Teams).
- Find [early adopters and champions](https://adoption.microsoft.com/roles/champion/) and create ways to extend their enthusiasm to the rest of the organization.
- Plan to engage with users where they typically meet and share information (for example, if your organization already meets in Teams, plan to post in channels.)
- Determine who and where questions about Viva Connections should go to. Consider using [Viva Engage](https://support.microsoft.com/office/join-and-create-a-community-in-yammer-56aaf591-1fbc-4160-ba26-0c4723c23fd6), a [SharePoint site](https://support.microsoft.com/office/create-a-site-in-sharepoint-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8), or a [Teams channels](https://support.microsoft.com/office/create-a-channel-in-teams-fda0b75e-5b90-4fb8-8857-7e102b014525) allow users to ask questions or see commonly asked questions.

### Change management considerations

- Start by creating awareness and interest in multiple channels to appeal to different audiences. Consider common spaces for on-site users like the break room or conference rooms. For remote workers and the rest of the organization, plan to post announcements in Teams, Viva Engage, and SharePoint.
- Make sure different audiences of end-users can easily understand how this new tool will help improve their day-to-day work.
- Create opportunities for users to ask questions, get help, and see live demonstrations. Consider setting up weekly training sessions or office hours during the first month of adoption. Use champions where possible.
- Reinforce change by creating incentives for using the new tools.
- Clearly explain how to use Viva Connections on desktop and mobile apps, how to engage with the Dashboard, the Feed, and Resources, and where to view the latest news and announcements.
- Create specialized guidance for different audiences like frontline workers or hybrid workers.

### Training considerations

- Use training to help raise awareness about where resources [can be accessed in Teams on desktop or mobile devices](https://support.microsoft.com/topic/3da30f39-684a-4bde-bb81-2e1407d59b52).
- Showcase different ways to connect and engage with cards on the dashboard and content in the Feed. Consider providing different training guidance for different audiences.
- Highlight popular portals in SharePoint that can be found in the Resource tab when on a mobile device.

#### Adoption resources

Learn more about adoption, best practices, and get communication templates in the [Viva adoption center](https://adoption.microsoft.com/viva/).

## Step 7: Consider success metrics

Part of the planning process includes determining which metrics will be used to measure how effective Viva Connections is in bringing your organization together and keeping specific audiences informed. Start by considering the tasks and tools that the dashboard will offer. For example, if you create a card that links to your human resources SharePoint site or a specific page, you should expect to see more traffic and engagement for that site in usage reports.

> [!NOTE]
>
> The analytics feature is unavailable in GCC, GCC High, and DoD environments. Please refer to the [list of service availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#service-availability-for-each-plan) for more information.

- **Viva Connections analytics:** Understand how and when users engage with components of the Viva Connections experience by using [Viva Connections analytics](viva-connections-analytics.md). Review the number of people who have viewed and engaged with Viva Connections experiences, the content types users engage with, and the platforms used to access Viva Connections.
- **High-level view of usage across M365 apps:** Use [Microsoft 365 usage analytics](/microsoft-365/admin/usage-analytics/usage-analytics) to access a pre-built dashboard that contains several pre-built reports that focus on adoption of M365 apps, usage, communication, and collaboration.
- **Site or page level data:** Get [site level](https://support.microsoft.com/office/view-usage-data-for-your-sharepoint-site-2fa8ddc2-c4b3-4268-8d26-a772dc55779e) and [page level](https://support.microsoft.com/office/view-usage-data-for-pages-and-news-e3186199-ccc8-4445-9162-bb1bcec8b7ee) usage reports in SharePoint to gauge engagement and learn more about when users access content and what devices they're using.
- **Get direct feedback from users:** Usage analytics aside, you can ask users directly about their overall satisfaction. Consider [creating a card on the Dashboard that links to a Microsoft Form](https://support.microsoft.com/office/create-a-form-with-microsoft-forms-4ffb64cc-7d5d-402f-b82e-b1d49418fd9d) where you can ask users to rate satisfaction and provide feedback.

## Step 8: Plan for maintenance over time

Generally, Viva Connections needs minimal ongoing maintenance once it's set up. As your business grows and evolves, you'll likely identify new scenarios that can be supported by Viva Connections. Over time, you may decide to retire cards on the dashboard or rearrange global navigation in resources. Additionally, users will share feedback that can be used to improve the experience. Each of these scenarios will require time to implement and to communicate as needed. Plan to have a point-person, or team of people, who can manage these tasks over time.  

- **Dashboard:** Once designed and tested, the dashboard will only need to be updated to support new scenarios or retire old scenarios.
- **Feed:** Content is dynamically displayed and aggregated from SharePoint news posts and Viva Engage.  
- **Resources:** Like the dashboard, once links to portals have been established, the Resources will only need updates as needed.

## Next, build and customize Viva Connections for your organization

After you meet requirements (for customers who want a SharePoint home site), have a plan for the dashboard, and are prepared to help users adopt Viva Connections, it's time to [move on to the build phase](build-viva-connections.md).
