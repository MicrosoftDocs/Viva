---
ms.date: 11/15/2022
title: Organization insights in the Viva Insights app
description: Find Organization insights in Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Organization insights in Viva Insights

Organization insights help leaders and managers of large teams understand how their organizations—the people who report to them directly or indirectly—are succeeding at work. Leaders and managers can see key indicators of their organization’s wellbeing, productivity, and team culture, and they can find features and tools to help support their teams.

## Subscriptions, roles, and access

To view organization insights:

* You need to have a Viva Insights subscription (that is, a premium license).
* Your Insights admin needs to assign you the [**Insights Business Leader** role](../advanced/setup-maint/assign-user-roles.md) or enable you as a [group manager](../advanced/setup-maint/manager-settings.md#to-configure-manager-settings) in Viva Insights. 
* You need to have a number of direct and indirect reports that meets or exceeds the [minimum group size](../advanced/setup-maint/manager-settings.md#to-configure-manager-settings) your Insights admin set. 

People in your organization also need to have a Viva Insights subscription so they can be measured in organizational insights. These employees are referred to as "measured employees." If you want to see an insight that reflects your entire company, everyone in the company needs to have a Viva Insights subscription.

### Insights by role

People with the **Insights Business Leader** role assigned to them can access organization insights that include every measured employee in their tenant. 

People enabled as group managers can access organization insights that include people who report to them directly or indirectly. Your Insights admin maintains this reporting hierarchy. If your admin assigned you the **Insights Business Leader** role and also enabled you as a group manager, you can toggle between the two organization insights views.

## Data and privacy

Viva Insights commits that no user will discover information about another identified individual that they couldn't already know. This principle applies to every feature in Viva Insights, including organization insights.

For further detail about privacy and organization insights, refer to our [privacy information](../advanced/privacy/privacy.md).

## Using organization insights

Organization insights are more than just a dashboard—they also provide helpful features to share insights and actions with your organization. Here's what you might see when you open your Viva Insights app:

:::image type="complex" source="images/org-insights-all2.png" alt-text="Screenshot that shows the organization insights section." lightbox="images/org-insights-all2.png":::
   Screenshot of the "Your organization insights" section in the Viva Insights app. The image shows three insight cards. From left to right: "Uninterrupted focus hours," which is the largest, "Multitasking hours," and "Meeting hours." Elements of the organization insights section are labeled with numbers 1-5, which correspond to feature description labels below. 1 is the scope selector, currently labeled "Your company," in the top right corner. The rest of the labels are on the "Uninterrupted focus hours" insight card. 2 is the indicators, placed next to the text, "0.3 hours per person last week." 3 is the "Show details" link next to the "Set up plan" button at the bottom left of the card. 4 is the share button at the bottom right of the card. 5 is the "Set up plan" button.
:::image-end:::

Let's take a look at how to use these features:

1. **Scope information** 

     At the top-right of any page or section with organization insights, an indicator shows how many people the insights are measuring. If you're enabled as a group manager *and* you have the **Insights Business Leader** role assigned, you can use this toggle to view insights for either your reporting organization or for the entire company.

    The measured group reflects people who:

    * Are in your reporting hierarchy, based on the organizational structure that your Insights admin maintains.
    * Have a Viva Insights subscription (that is, a premium license) applied to their account.
    * During the week that the insight is generated for, were active in Outlook or Teams.

    People need to meet *all* of these criteria to be part of the measured group reflected here—that is, your scope. Select the tooltip on the toggle to view this criteria while you're viewing insights.

1. **Indicators**

    Insight indicators show you your organization’s average for the most recent period available, and how much it has changed from the period prior. 

1. **Details**

   **Insight details** is your jumping-off point to explore context about your measured results. When you select **Show details**, Viva Insights brings you to the insight drill-down page. This page contains information like trend lines, peer comparisons, comparisons across groups within your organization, and distributions.

    >[!Note] 
    >About comparisons across groups: if a team that reports into you doesn't meet the minimum group size set by your Insights admin, then granular data for that team won't be available.

1. **Sharing** 

    Sharing is available for most insight cards. You can share an insight in one of two ways:
    * **In a Teams chat** – When you share through a chat, you'll have the option to send a screenshot of the insight to another person and add a custom message. The chat contains a link, so the recipient can view how the insight looks for their own team. Recipients need to qualify for organization insights to be able to view what you share with them here.
    
        :::image type="complex" source="images/org-insights-share-chat1.png" alt-text="Screenshot that shows sharing an insight by chat.":::
           Screenshot of the "Share via chat" window. The title reads, "Start adding people to share." Beneath the title is a "Send to" field where users can add recipients. This field currently contains a recipient, showing their profile image and name, with an X button to cancel. Beneath "Send to" is a "Leave a note" field which includes user-entered text. Beneath "Leave a note," a box next to the text, "Include a preview of my own insight" is checked. In the bottom portion of the window, there's a "Preview" section that shows what the recipient will see. The message title reads, "Elvia Atkins shared insights with you." Below the message title, there's the note the sender wrote above. Part of the insight is visible in the preview. In the bottom right of the window, there's a "Done" button.
        :::image-end:::

    * **Through a link** – When you share through a link, that link takes the recipient to the same location in Viva Insights. Linking someone doesn't give them access to the same data you can see, but if they also have access to organization insights, they'll see results for their own group.


        :::image type="complex" source="images/org-insights-share-link.png" alt-text="Screenshot that shows sharing an insight by link.":::
           Screenshot of copying an insight link. The image shows a checkmark and a label with the text, "Link to 'Uninterrupted focus hours' copied." Below the label is a web address field; this address field contains a direct URL to the insight. To the right of the address field, there's a "Copy again" button. In the top right of the window, there's an X button to close the window.
        :::image-end:::
1. **Actions**

    Actions point you to other workflows in Viva Insights that can help support you or your organization to manage a measured behavior. 

    Here's an example:

    Let's say an insight shows people's meeting time has significantly increased. The insight card might contain a button to set up a plan. When you select the button, Viva Insights takes you to the [no-meeting day plan](../personal/teams/shared-no-meeting-day.md) to help folks dedicate a full day to their independent work.

## Insights per tab

### Home

On the **Home** tab, you'll find key indicators of your organization’s wellbeing, productivity, and team culture, along with features and tools to help support your teams. 

Specifically, you'll find an insight related to one of the following topics each day:

* Uninterrupted focus hours
* Manager 1:1 meeting hours
* Meeting hours
* After hours collaboration
* No meeting day impact
* Daily connected hours
* Focus time participation
* Join on time rate
* Focus time impact
* No meeting day participation
* Multitasking hours
* Internal network size

All insight cards show the current week's average measure, and also provide the difference from the prior period. Here's an example:

:::image type="complex" source="../personal/teams/images/home-org-insight-example.png" alt-text="Screenshot that shows an organization insight on the Home tab.":::
   Screenshot that shows an organization insight card on the Home tab. The insight includes a title, subtitle, numerical indicator, increase/decrease indicator, a line graph, and a recommended action with a button to begin that action, which is to set up a no-meeting day. There's also a "Show details" link and a share icon.
:::image-end:::

### Wellbeing

On the **Wellbeing** tab, you'll find key indicators of your organization's capacity for focused work and work-life balance.

Each day, an insight related to one of the following topics appears at the top of your **Wellbeing** tab:

* Uninterrupted focus hours 
* After hours collaboration 
* No meeting day impact
* Daily connected hours 
* Focus time participation 
* Focus time impact 
* No meeting day participation

On the insight card, view the current week's average measure, the difference from the prior period's average, and the measure's 12-week trend. 

:::image type="complex" source="../personal/teams/images/wellbeing-org-insights.png" alt-text="Screenshot that shows an uninterrupted focus hours organization insight at the top of the Wellbeing tab.":::
   Screenshot of the "uninterrupted focus hours" organizational insight on the Wellbeing tab. The title of the page reads, "Uninterrupted focus hours - is there time for individual work?", with an information icon to the right. Below the title is a numerical indicator of "13.0 hours per person last week" with a text denoting an increase by 1.6 hours. To the right of the indicator is a line graph with months on the X axis and hours, increasing in intervals of 10, on the Y axis. Below the indicator and graph, there's a label with the text, "A shared focus plan invites your team to protect time to get work done." Below the text is a "Set up plan" button and "Show details" link. In the top right of the screen, there's a scope selector indicating that data is being shown for the organization.
:::image-end:::

If you want more information about the insight, including a comparison to peer organizations (for eligible users), a breakdown by team, a percentage distribution, and calculation methods, select **Show details** on the insight card.

:::image type="complex" source="../personal/teams/images/wellbeing-org-insights-detail.png" alt-text="Screenshot that shows the insight detail page for Uninterrupted focus hours.":::
    Screenshot of the Details page for the "Uninterrupted focus hours" insight. The page shows a numerical indicator for the organization and another numerical indicator for peer organizations. Descriptors sit beneath the organization and peer indicators and both contain tooltips. Below the descriptions is a line graph with months on the X axis and hours, in increments of two, on the Y axis, along with a color key indicating "Your organization" and "Peer organization." Below the line graph, there's a "Snapshot from last week" donut chart, which shows a percentage of employees who could benefit from more focus time. There's also a "Percentage of your organization" bar chart, with hours of focus time on the X axis and percentage on the Y axis. On the right of the screen is a card titled, "Block time for focus" that allows users to start a shared focus plan. The card contains a "Set up plan" button and "More actions" links. In the top right of the screen, there's a scope selector indicating that data is being shown for the organization.
:::image-end:::


To help your team improve their wellbeing, Viva Insights shows you a recommended action—for example, starting a shared focus plan. Select the action button, like **Set up plan**, either on the insight card on the **Wellbeing** tab, or from within the insight details page. Viva Insights then takes you through the feature setup process.

You can also access shared actions in your **Take action to improve your wellbeing** section. Start a shared focus plan or a [shared no-meeting day](shared-no-meeting-day.md).

### Productivity

On the **Productivity** tab, you'll find key indicators of your organization’s meeting effectiveness, along with features and tools to help support your teams.

Each day, an insight related to one of the following topics appears at the top of your **Productivity** tab:

* Meeting hours
* Join on time rate
* Multitasking hours

>[!Tip]
>To find other insights, use the arrows to the right of the **Your organization/Your company** dropdown.

On the insight cards, view the current week's calculation result and the change over time for your organization or the group of people who report to you directly or indirectly. If you want more information about the insight, including a comparison to peer organizations (for eligible users), a breakdown by team, a percentage distribution, and calculation methods, select **Show details** on the insight card.

Some insight cards also provide recommended actions. For example, to help your team improve their meeting effectiveness, you can choose to set up a no-meeting day. Select the action button, like **Set up plan**, either on the insight card on the **Productivity** tab, or from within the insight details page. Viva Insights then takes you through the feature setup process.  

:::image type="content" source="../personal/teams/images/productivity-org-insight-trend.png" alt-text="Screenshot that shows a meeting hours organization insight at the top of the Productivity tab.":::

### Teamwork

You’ll see a **Teamwork insights for your organization** section at the top of your **Teamwork** tab. Each day, you’ll receive an insight about internal network size across your organization or company. 

## Related information

### Helpful terms

* <a name="current-period-define"></a> **Current period** – Unless otherwise stated, most insights are showing the result for the most recent period—that usually means the most recent complete week of data. A few insights use a four-week or rolling four-week window instead, to smooth normal variability and make it easier to understand the insight. If an insight uses something other than the most recent week for the current period, you will see it called out on the insight card. 
* <a name="employees-define"></a> **Employees** – Organization insights provide measures for groups of employees, and are meant to capture what typical workday activity looks like for those employees. To avoid skewing the averages by including people who are not at work during the week (for example, they are on holiday or out sick), organization insights only measure people who have some activity in Outlook or Teams during the week.
* <a name="organization-breakdown-define"></a> **Organization breakdown** – The groups displayed in the organization breakdown are based on your reporting hierarchy, which your Insights admin [maintains](../advanced/setup-maint/setup.md#prepare-and-upload-organizational-data). Each group includes people who report directly or indirectly to a person who reports to you. The insights represent the activity of the group, not just that person who reports to you, even though their name is used to label the group. 

    Insight Business Leaders who are viewing the insights for the entire company will see the organization breakdown by organizations reporting to top-layer leaders.
* <a name="peer-organization-define"></a>**Peer organization** – Peer organization includes groups near your own group in the reporting hierarchy. If available, the peer organization includes people who report directly or indirectly up to your manager, but not up to you. If there aren't any groups like this, or they don’t meet the minimum group size, the peer organization includes people who report directly or indirectly up to your skip-level manager but not up to you. If there’s not enough people who meet that definition either, you won't see peer organization insights. 

    Insights Business Leaders who are viewing insights for the entire company will also not see peer organization insights.
* <a name="prior-period-define"></a>**Prior period** – The prior period is the period immediately before the most recent period – usually the week before the most recent completed week. 
* <a name="reporting-hierarchy-define"></a>**Reporting hierarchy** – Your Insights administrator manages the reporting hierarchy. This hierarchy identifies reporting relationships throughout the company: people who are managers, and the people who report to them. The reporting hierarchy might be sourced from Azure Active Directory or from a manual upload from your company’s HR information system. Viva Insights uses this information to identify people in your organization, your peer organization, and any organizations that might report up to you.
* <a name="your-organization-define"></a>**Your organization** – If the insight scope selector says **Your organization**, this group includes everyone who reports to you directly or indirectly. This group is based on your organization’s reporting hierarchy, your Insights administrator manages. If the insights scope selector says **[Your company name]**, this group includes everyone who has been set up as part of the premium insights group by your Insights administrator.

## Metric definitions

The following table lists metrics related to organization insights. You can also access metric definitions while you're using Viva Insights—just select the (i) icon next to the organization insight card or organization insight page title.

Refer to [Metric definitions](../advanced/reference/metrics.md) for all Viva Insights metric definitions.
 
|Metric	| How it’s calculated|
|--------|--------------------|
After-hours collaboration hours	| After-hours collaboration measures how much time per week a person spends in meetings, emails, Teams chats, and Teams calls outside of their configured working hours.
Uninterrupted focus hours | Uninterrupted focus hours measures blocks of time longer than an hour where the person is not in a meeting or Teams call or sending email or Teams chats. 
Daily connected hours | Daily connected hours measures time in 30-minute blocks in a day where the person had any activity where they took a meeting or Teams call or sent an email or Teams chat.
|Collaboration hours | Collaboration hours measures the total time per week a person spends in meetings, emails, Teams chats, and Teams calls. 
|Meeting hours | Meeting hours measures the total time per week a person spends in meetings based on accepted meetings on their Outlook calendar and excluding calendar items that are likely non-meetings, such as appointments.
|Join on time rate	| Join on time rate measures the percentage of Teams meetings where the person joined early or within five minutes of the meeting’s scheduled start time.
| Recurring meeting hours | Recurring meeting hours measures the total time per week a person spends in recurring meetings based on accepted meetings on their Outlook calendar and excluding calendar items that are likely non-meetings, such as appointments.
|Large and long meeting hours| Large and long meeting hours measures the total time per week a person spends in meetings that are longer than an hour or have more than 8 attendees.
|Multitasking hours	| Multitasking hours measures how much time per week a person spends in emails and chats that overlap with their meetings and Teams calls.
|Manager 1:1 meeting hours| Manager 1:1 meeting hours measures how much time a person spends in meetings with just themselves and their direct manager. This is calculated over a rolling four-week period. 
|Internal network size|Internal network size measures the number of colleagues connected to the person. Connections are based on at least two interactions in the prior four-week period, excluding very large and long interactions. 
|Manager co-attendance rate	| Manager co-attendance rate measures what percentage of meeting hours are attended by both the person and the person’s direct manager.


