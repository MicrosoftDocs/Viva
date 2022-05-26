---
title: "Plan Viva Connections for your organization"
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
description: "Plan Microsoft Viva Connections for your organization"
---

# Plan Microsoft Viva Connections for your organization




### Step 1: Meet requirements
Viva Connections requires a SharePoint home site, customized global navigation in the SharePoint app bar, and modern SharePoint sites. 


| Requirement    | Description                 | 
| :------------------- | :------------------- |
| Create a home site  | A home site is a SharePoint communication site that acts as the front door to your organization’s intranet. [Home sites](/sharepoint/home-site-plan) are SharePoint communication sites that have extra capabilities such as the ability to prioritize news posted from the home site across the rest of the intranet. Once a home site is set, the news posted from that site will be prioritized across the intranet. <br> <br> Learn more about how to think about [planning navigation on your home site](https://techcommunity.microsoft.com/t5/microsoft-sharepoint-blog/best-practices-for-using-global-navigation-in-the-sharepoint-app/ba-p/2361916) in combination with hub and global navigation. Then, get started [creating a home site](/sharepoint/home-site-plan). | 
| Set up global navigation |Once your home site is set up, you can enable and customize global navigation in the SharePoint app bar. Global navigation can only be edited by the site owners of the home site. In the Viva Connections desktop app, resources in the global navigation will display when the Viva Connections icon is selected in Teams. In the Viva Connections mobile app, resources in the global navigation will display in the “Resources” tab. <br><br> Learn more about how to [enable and customize global navigation](/sharepoint/sharepoint-app-bar). | 
| Audit, prioritize, and modernize sites | After you've identified the key scenarios for Viva Connections, you’ll need to identify content or sites that should be modernized if you're still using classic sites and pages. Not all content or classic SharePoint sites need to be modernized to take advantage of Viva Connections. Focus on the priority use cases that will need to be included in your organization’s instance of Viva Connections. <br><br> Learn more about [how to modernize content](/sharepoint/dev/transform/modernize-classic-sites#:~:text=Modernize%20your%20classic%20SharePoint%20sites%201%20Enable%20your,site%20transformation%20is%20transforming%20your%20site%20pages.%20) and [healthy portal guidance for high-traffic sites](/sharepoint/portal-health)| 

#### Create a home site for your organization (required)
Viva Connections requires a [SharePoint home site](/viva/connections/home-site-plan) which is a communication site that has special capabilities. A home site is the front door to your organization’s intranet and a gateway to other popular portals that are relevant to the entire organization. Your home site will also be the landing experience for Viva Connections in the Microsoft Teams desktop app. 

   ![Image of Viva Connections desktop.](../media/connections/viva-connections-desktop.png)

Start small by identifying a handful of resources and functions that the home site can serve. Consider using a [customizable site template from the SharePoint look book called The Landing](https://lookbook.microsoft.com/details/c9300e94-6e83-471a-b767-b7878689e97e) to quickly get your home site up and running. Optionally, turn your home site into a [SharePoint hub site](/sharepoint/planning-hub-sites) to add an extra layer of navigation and increase the search scope. 

Learn more about [how to plan your home site](/sharepoint/home-site-plan) and [how to launch healthy SharePoint sites](/sharepoint/portal-health). 



#### Set up global navigation in the SharePoint app bar (required)
Next, from the home site Settings icon, select [Set up global navigation](/SharePoint/sharepoint-app-bar) to take advantage of full Viva Connections functionality. Design global navigation in a way that compliments and expands resources on the home site. [Learn more about navigation and information architecture in SharePoint](/sharepoint/information-architecture-modern-experience).

   ![Animation of the global app bar in SharePoint.](../media/connections/app-bar-gif.GIF)


Navigational links that appear in the global navigation pane in the SharePoint app bar will also display in the Viva Connections app in Microsoft Teams for desktop and mobile apps. 


#### Audit, prioritize, and modernize content to align with key scenarios and tasks (optional)
After defining the key scenarios and tasks in the planning phase, prepare for Viva Connections by ensuring priority content is located on modern SharePoint communication sites and team sites. Only modern sites will appear in the Microsoft Teams app. Classic sites will open in a separate browser window.

If you have many classic SharePoint sites make sure you focus on sites, pages, and content that are relevant to the Viva Connections experience. Sites and content that are unrelated to key tasks and scenarios can be modernized later.

**Sites that should be audited and prioritized:**
   - Sites that connect to cards on the Viva Connections Dashboard
   - Sites that are displayed in global navigation
   - Sites that frequently publish organizational news
   - Sites that help employees complete the most important day-to-day tasks or access important information

**Tools to help you modernize:**
   - Use the [SharePoint modernization scanner](/sharepoint/dev/transform/modernize-scanner) to create a dashboard that helps you determine modernization readiness. 
   - Learn more about how to [transform classic sites to modern sites](/sharepoint/dev/transform/modernize-userinterface-site-pages), or consider [creating new modern sites using SharePoint site templates](https://support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398). 
   - For popular sites that are expected to get a high amount of traffic (thousands of views per day) [learn more about best practices for high-performing sites and portals](/sharepoint/portal-health).


## Step 2: Plan for Viva Connections
Viva Connections is designed to help users complete high-priority tasks and access important information. This experience can be built on overtime as your organization adapts and scales. 

Viva Connections is composed of three main parts – the Dashboard, the Feed, and Resources. These parts will display differently on desktop and mobile devices. [Learn more about the differences between the desktop and mobile experience](/connections/viva-connections-overview). 

- **Dashboard:** The Dashboard is your employee’s digital toolset. It brings together the tools your employees need, enabling quick and easy access whether they are in the office or in the field. 
- **Feed:** The Feed delivers updates to the right people at the right time and is tightly integrated with Yammer, SharePoint news, and Stream to display a personalized feed, based on post-level targeting of the groups that employees belong to. 
- **Resources:** The Resources experience enables way finding across platforms. It uses navigation elements from the SharePoint app bar, which can be [audience targeted](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293).


| Desktop              | Mobile              | 
| :------------------- |:------------------- |
| ![Image of the Viva Connections landing experience in the desktop app.](../media/connections/teams-desktop-small.png)|![Image of the Viva Connections landing experience in the mobile app.](../media/connections/mobile-dashboard-small.png)| 
|- Your organization’s instance of Viva Connections [will appear as an icon](/viva/connections/add-viva-connections-app#then-customize-the-app-settings) in the Teams app bar. <br> - When the icon is selected, users will see the home site in Teams. <br> - When the icon is selected twice, the global navigation panel will display. <br> - Add the [Feed web part](use-feed-web-part-for-viva-connections.md) to highlight personalized news. <br> - Add the [Dashboard web part](use-dashboard-web-part-on-home-site.md) to make it easy to complete tasks | - Your organization’s instance of Viva Connections will appear as an icon in the Teams mobile app bar. <br> - Once selected, users can pivot from the Dashboard to the Feed to Resources. <br> - Resources come from global navigation. |



### Step 3: Plan the Dashboard
Start by identifying the key scenarios that Viva Connections needs to support and identify owners of those employee experiences. Tasks and scenarios will be primarily supported by cards in the Viva Connections Dashboard that can be targeted to specific audiences using Microsoft 365 groups. Consider which groups of employees will need access to specific resources. 

| Dashboard animation  | Description                 | 
| :------------------- |: ------------------- |
| ![Interaction between the Dashboard and cards.](../media/connections/new-vc-dashboard-interaction.GIF) | In this example, a card on the Dashboard is linked to a SharePoint page where users can take a daily health check easily from a mobile device.| 


Common scenarios include view paystubs and vacation hours, submit help tickets, catch up on news, check daily lunch menus, find people in a directory, and shift management. Collaborate and align with business groups that manage these experiences to determine the best design.


**Popular scenarios that can be supported by Viva Connections:**

| General | For information workers   | For frontline workers  |
| :------------------- | :------------------- |:-------------------|
| - View pay and benefits <br> - Submit a ticket to the help desk <br> - Access lunch and café options <br> - Catch up on news and announcements | - Find people and team information <br> - Complete required training <br> - View company holidays | - View and manage shifts <br> - Access time sheets and popular forms <br> - View workplace policies and resources | 

#### Types of Dashboard cards:
As you plan, consider the different types of cards available. There are three different types of cards that can be used on the Viva Connections Dashboard. Some cards may take longer than other to implement or may require work on the backend to set up.
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
As a best practice, it's important to make decisions that are rooted in specific tasks for certain audiences. Consider using a common framework for scenario planning that starts by selecting a certain role or audience *"As an..."*. Then, narrow down the objective in *"I need to..."*. Next, consider the ideal tool or process to meet the objective in *"So that I..."*. Lastly, script out what success looks like in *"I know this is successful when..."*.

For example, create a table like the following to list business scenarios that you want to address with cards in the Dashboard:

|**As an...**|**I need to...**|**So that...**|**I know this is successful when...**|
|:-------------------|:---------------|:-----------|:------------------------------------|
|People manager |Welcome and onboard new team members |I can grow and develop talent |I spend less time managing standard onboarding functions |
|Sales representative| Access specific product training materials while on a mobile device |Can quickly resolve customer issues|Most customer issues get resolved in real-time|
|HR specialist |Promote the use of the self-service benefits |I can spend more time working with employees on unique benefits questions and scenarios|All of my employee interactions are about individual critical scenarios|



#### Examples of different Dashboard designs
The Dashboard should focus on the most important tasks. Tasks that are specific to certain audiences should be targeted to make sure users only see cards that are relevant to their day-to-day jobs.

| Information workers   | Frontline workers  | 
| :------------------: |:------------------: |
| ![Image of the Viva Connections dashboard designed for frontline workers.](../media/connections/dashboard-information-worker.png) |  ![Image of the Viva Connections dashboard designed for information workers.](../media/connections/dashboard-frontline.png) | 


#### Planning resources:
- [Create and customize a Dashboard](/viva/connections/create-dashboard)
- Learn more about [adaptive cards](https://adaptivecards.io/)and  [third-party cards](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/viva-connections-welcomes-new-partners-and-opens-developer/ba-p/2540643)
- Use existing [Microsoft 365 groups](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) or create news groups if needed so that you can quickly create cards and [target them to specific audiences](/viva/connections/create-dashboard#apply-audience-targeting-to-cards)


### Step 4: Get ready for the Feed
The Feed brings communications from across the organization into one place where it can be easily viewed. This Feed helps keep frontline workers, information workers, and hybrid workers alike engaged and informed on important news and announcements. This solution also gives content publishers a reliable method of distributing important news and information. Technically, you do not need to do anything to set up the Feed because content will sync automatically. However, you can influence the content hierarchy. 

![Image of the Feed in the mobile app.](../media/connections/mobile-feed.png) 


#### Tips on how to influence content hierarchy in the Feed:
The Feed is designed to be dynamic, personalized, and a place where the most relevant news and announcements can be consumed. The Feed relies on a constant flow of new content and the best experience contains a balance of organizational news, organic content, and curated content.
-  Publish SharePoint news from [official organizational news sources](/sharepoint/organization-news-site#:~:text=Use%20Microsoft%20PowerShell%20to%20specify%20a%20site%20as,organization%20news%20site%3A%20PowerShell%20Set-SPOOrgNewsSite%20-OrgNewsSiteUrl%20%3Csite%20URL%3E) like the [home site](/viva/connections/home-site-plan)
- [Use News boost to elevate the most important news](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83#:~:text=1%20On%20your%20organization%20news%20site%2C%20open%20the,post%20to%20stop%20being%20boosted.%20More%20items...%20) posts on organizational news sites to surface news posts to the top of the feed
- [Post news as a video news links](/viva/connections/video-news-links) hosted by stream to share updates, rebroadcast an all-hands meeting, or provide reusable training materials
- Highlight community discussions by [featuring posts in public Yammer communities](/yammer/manage-yammer-groups/yammer-all-company-yammer-community) that you’d like seen by the entire organization
- Encourage your organization to [engage and participate in Yammer discussions](https://adoption.microsoft.com/yammer/), especially leaders and workplace champions
- [Use audience targeting](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293) to make sure specific content is seen by different audiences using Microsoft 365 groups


#### Planning resources:
- Review [frequently asked questions about the Feed](/viva/connections/faqs-viva-connections-feed) for Viva Connections
- Consider using the [Feed web part](https://support.microsoft.com/office/use-the-feed-web-part-for-viva-connections-001fbe90-3778-4801-9ea9-71308711d330#:~:text=%20Add%20the%20Viva%20Connections%20Feed%20web%20part,for%20Viva%20Connections%20Feed%20web%20part.%20More%20) on popular SharePoint pages to surface news and announcements


### Step 5: Plan the Resources
Resources are the navigational links to portals that get set up when you enable and customize global navigation. While preparing your Viva Connections, know that these resources will display from the SharePoint app bar and the Teams app bar when Viva Connections is set up. The resources in the app bar should be the most important and popular portals for your target audience. Resources can be targeted to specific audiences.

| Desktop             | Mobile                 | 
| :------------------: |: ------------------: |
| ![Image of global navigation in the desktop app.](../media/connections/vc-resources-small.png)| ![Image of global navigation in the mobile apps.](../media/connections/mobile-resources-small.png)| 


Consider how links in the global navigation will complement resources highlighted on the home site. Depending on the content you want to make available in the global navigation, you can [design your home site navigation and global navigation in three different ways](/viva/connections/sharepoint-app-bar#see-all-the-different-ways-you-can-set-up-global-navigation).


#### Planning resources:
- Set up for the first time, or [customize navigational links in the global navigation](/viva/connections/sharepoint-app-bar) from the home site
- Get more guidance on how to [design navigation in SharePoint](/sharepoint/information-architecture-modern-experience)



## Step 6: Create an adoption plan 
Planning for change and helping users adopt new resources will be different for every organization. Use the considerations and best practices here as a starting point to creating an adoption plan that fits your organization’s needs. Include considerations for change management and training materials for end-users in your plan.

### Adoption considerations:
- Viva Connections can only be accessed in Microsoft Teams. If your organization isn't already using Microsoft Teams, you'll need to [plan the adoption of Microsoft Teams](https://adoption.microsoft.com/microsoft-teams/) alongside [Viva Connections](https://adoption.microsoft.com/viva/).
- Make adoption easy for end-users by [pre-installing and pre-pinning the app in Teams](/viva/connections/add-viva-connections-app#then-customize-the-app-settings) while picking settings.
- Find [early adopters and champions](https://adoption.microsoft.com/roles/champion/) and create ways to extend their enthusiasm to the rest of the organization.
- Plan to engage with users where they typically meet and share information (for example, if your organization already meets in Teams, plan to post in channels.)
- Determine who and where questions about Viva Connections should go to. Consider using a [Yammer community](https://support.microsoft.com/office/join-and-create-a-community-in-yammer-56aaf591-1fbc-4160-ba26-0c4723c23fd6), [SharePoint site](https://support.microsoft.com/office/create-a-site-in-sharepoint-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8), or [Teams channels](https://support.microsoft.com/office/create-a-channel-in-teams-fda0b75e-5b90-4fb8-8857-7e102b014525) allow users to ask questions or see commonly asked questions.

### Change management considerations:
- Start by creating awareness and interest in multiple channels to appeal to different audiences. Consider common spaces for on-site users like the break room or conference rooms. For remote workers and the rest of the organization, plan to post announcements in Teams, Yammer, and SharePoint.
- Make sure different audiences of end-users can easily understand how this new tool will help improve their day-to-day work.
- Create opportunities for users to ask questions, get help, and see live demonstrations. Consider setting up weekly training sessions or office hours during the first month of adoption. Use champions where possible. 
- Reinforce change by creating incentives for using the new tools. 
- Clearly explain: how to use Viva Connections on desktop and mobile apps, how to engage with the Dashboard, the Feed, and Resources, and where to view the latest news and announcements
- Specialized guidance for different audiences like frontline workers or hybrid workers


### Training considerations:
- Use training to help raise awareness about where resources [can be accessed in Teams on desktop or mobile devices](https://support.microsoft.com/topic/3da30f39-684a-4bde-bb81-2e1407d59b52).  
- Showcase different ways to connect and engage with cards on the Dashboard and content in the Feed. Consider providing different training guidance for different audiences. 
- Highlight popular portals in SharePoint that can be found in the Resource tab when on a mobile device.


#### Adoption resources:
Learn more about adoption and get communication templates in the [Viva adoption center](https://adoption.microsoft.com/viva/).



## Step 7: Consider success metrics
Part of the planning process includes determining which metrics will be used to measure how effective Viva Connections is in bringing your organization together and keeping specific audiences informed. Start by considering the tasks and tools that the Dashboard will offer. For example, if you create a card that links to your human resources SharePoint site or a specific page, you should expect to see more traffic and engagement for that site in usage reports.

 - **High-level view of usage across M365 apps:** Use [Microsoft 365 usage analytics](/admin/usage-analytics/usage-analytics) to access a pre-built dashboard that contains several pre-built reports that focus on adoption of M365 apps, usage, communication, and collaboration. 
 - **Site or page level data:** Get [site level](https://support.microsoft.com/office/view-usage-data-for-your-sharepoint-site-2fa8ddc2-c4b3-4268-8d26-a772dc55779e) and [page level](https://support.microsoft.com/office/view-usage-data-for-pages-and-news-e3186199-ccc8-4445-9162-bb1bcec8b7ee) usage reports in SharePoint to gauge engagement and learn more about when users access content and what devices they're using. 
- **Get direct feedback from users:** Usage analytics aside, you can ask users directly about their overall satisfaction. Consider [creating a card on the Dashboard that links to a Microsoft Form](https://support.microsoft.com/office/create-a-form-with-microsoft-forms-4ffb64cc-7d5d-402f-b82e-b1d49418fd9d) where you can ask users to rate satisfaction and provide feedback.  


## Step 8: Plan for maintenance over time
Generally, Viva Connections needs minimal ongoing maintenance. This is partially because most resources and content are stored in SharePoint. Therefore, if your SharePoint intranet is up to date, so is Viva Connections. 
- **Dashboard:** Once designed and tested, the Dashboard will only need to be updated to support new scenarios or retire old scenarios.
- **Feed:** Content is dynamically displayed and aggregated from SharePoint news posts and Yammer communities.  
- **Resources:** Like the Dashboard, once links to portals have been established, the Resources will only need updates as needed.

As your business grows and evolves, you'll likely identify new scenarios that can be supported by Viva Connections. Over time, you may decide to retire cards on the Dashboard or rearrange global navigation in Resources. Additionally, users will share feedback that can be used to improve the experience. Each of these scenarios will require time to implement and to communicate as needed. Plan to have a point-person, or team of people, who can manage these tasks over time. 


## Next, build and customize Viva Connections for your organization
After you meet requirements, have a plan for the Dashboard, and are prepared to help users adopt Viva Connections, its time to [move on to the build phase](build-viva-connections.md). 

