---

title: Personal insights deployment guide
description: Guide for admins on deploying personal insights with Microsoft Viva Insights
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.service: viva 
ms.subservice: viva-insights 
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: helayne
audience: Admin

---

# Deploy personal insights

Personal insights with Microsoft Viva Insights is an easy-to-deploy, out-of-the-box solution that helps you and your co-workers improve your personal productivity habits. It is available widely &mdash; to Microsoft 365 users with [these Service plans](../overview/plans-environments.md). After licenses are assigned, the Viva Insights is turned **On** by default, although you can customize your deployment by [following the steps in this guide](#roll-out-viva-insights).

## What is Viva Insights?

To quickly learn about Viva Insights, checkout [Microsoft Viva Insights](https://www.microsoft.com/microsoft-viva/insights).

### Business value of Viva Insights

More people than ever feel they lack control over their time at work. Many teams spend 80-90% of their week sitting in meetings, sending emails, and talking on the phone. But 50% of meeting time is seen to be unproductive and almost half of employees report that their work interferes with their family life.

Viva Insights is an extension of your Microsoft 365 client experience that helps you find opportunities to build better habits and get back in control of your time. 

### Benefits of Viva Insights

By using Viva Insights, you and your team can accomplish great things.

* **Improve work patterns through personal productivity insights** - Viva Insights uses everyday data from Microsoft 365 to give you insights into how you spend your time and tips that help you work smarter.
* **Improve your relationships** - Increase your collaboration time, improve your team meetings, and grow your network.
* **Get more focus time** - Find more time to eliminate distractions, stop multi-tasking, and focus on your core priorities.
* **Improve your work-life balance** - Improve your work patterns and reduce the time you spend working for better work-life balance and overall wellbeing.

<!--### Case studies

* Discover how a large Fortune 500 customer used MyAnalytics to foster wellbeing and productivity: [How Fannie Mae uses MyAnalytics](https://customers.microsoft.com/story/809849-fannie-mae-case-study-banking-microsoft-365)
   
   For employees who are new to remote work during the COVID-19 pandemic, having access to colleagues and information through Microsoft 365 tools at any time of day has been critical to staying productive, while MyAnalytics helps them use work hours more effectively. "Using the Focus scheduling feature is helping people block off time on their calendars each day to knock out priority projects, which is especially helpful for our employees who are juggling family needs along with work." _- Dawn Damico: Vice President of Digital Workplace, Fannie Mae_

* Hear how the world's largest brewer used MyAnalytics in conjunction with Workplace Analytics to change its workplace collaboration habits for the better: [ABInBev](https://customers.microsoft.com/story/758970-ab-inbev-consumer-goods-workplace-analytics) 
   
  [![ABInBev.](../../images/mya/setup/ab-in-bev-video.png)](https://customers.microsoft.com/story/758970-ab-inbev-consumer-goods-workplace-analytics)

  _The use of MyAnalytics and Workplace Analytics at ABInBev_ 
-->
## Roll out Viva Insights 

You can deploy Viva Insights in your organization all at once or in phases. In either case, before you roll out the product broadly, we recommend that you obtain additional buy-in, an optional step that is described in the following [preparatory steps](#preparatory-steps) section.

### Viva Insights rollout checklist

1. (Optional) Complete the [preparatory steps](#preparatory-steps).
2. [Choose a rollout scenario](#choose-a-rollout-scenario).
3. Complete the steps in the rollout scenario that you chose.

### Preparatory steps

It is easy to turn on Viva Insights for all users in your organization as it comes with your [Microsoft 365 subscription](./../overview/plans-environments.md). Here is a list of recommended but optional steps that your organization might consider.

* **Create a communication plan** - Identify how your organization will effectively communicate with users during and after the rollout of Viva Insights. Make it easy for users to find information about Viva Insights. For example, use Yammer groups or SharePoint sites to help users learn about the benefits of using Viva Insights within their organization.
* **Consider your stakeholders** - It may be important in your organization to identify and communicate with stakeholders ahead of rollout of Viva Insights. See [Include stakeholders](#include-stakeholders). 
* **Consider running a pilot first** - Before scaling Viva Insights to your entire organization, you might want to consider [running a pilot rollout](#run-a-pilot-rollout) with a subset of users. Especially for large organizations, it is a natural step to test a broad rollout on a small scale first by conducting a pilot to validate user readiness, identify and mitigate issues, and help ensure a successful organization-wide implementation. 
* **Security and Privacy** - Viva Insights is secure and built to protect user privacy. The [Privacy guide](./../overview/privacy-guide-users.md) describes how Viva Insights complies with privacy regulations. We recommended that you share this privacy guide with security and privacy teams to give them a better understanding of the privacy features of Viva Insights.
* **Tie to existing initiative** - As you introduce Viva Insights, tie it to an existing initiative or training plan within your organization such as an employee wellbeing initiative. Avoid introducing it as a technology tool but rather as a habit-changing tool that is integrated with the organization’s values. 

### Include stakeholders

Identifying and notifying your key stakeholders before the welcome email is sent to users can be an important preliminary step in your rollout process. These stakeholders should understand the value, timelines, and expected experiences that come with the rollout of the Welcome email. When managed proactively, these stakeholders can become valuable advocates for moving the rollout process forward. 
<!-- need a new welcome email template - ([Download Welcome email template](/workplace-analytics/personal/setup/myanalytics-announcement-2020-template.docx)) -->

Here are some roles you might consider as part of the rollout project:

* **Executive sponsor** - Send welcome email about Viva Insights, ideally with quotes about their experience with the product.
* **Security lead** - Reviews the [Privacy guide](../overview/privacy-guide-users.md) to learn about data security in Viva Insights.
* **Microsoft 365 admin** - Enables and disables Viva Insights access per business requirements; see [Rollout scenarios](#rollout-scenarios). 
* **Support or Help desk lead** - Manages questions from users. Some helpful answers can be found in the [Viva Insights FAQs](./../overview/mya-faq.md).
* **Training lead** - Runs a training workshop. The lead can start with [Introduction to Microsoft Viva Insights](/training/modules/workplace-analytics-ways-working-action/) as a resource.

## Choose a rollout scenario

This section presents four scenarios for deploying Viva Insights. An Microsoft 365 admin can implement any of these scenarios either by using PowerShell or by using the Microsoft 365 admin center. Typically, admins use the admin center to broadly configure Viva Insights for most or all users, and they use PowerShell to set specific configurations for select users.

### Rollout scenarios

Select and complete one of the following scenarios:

* [Default on](#default-on). For all users, all surfaces of Viva Insights are turned on by default. This is the default scenario.
* [Default off](#default-off). Viva Insights is off by default; users can individually turn on some or all Viva Insights surfaces.
* [Mixed deployment](#mixed-deployment). Some users are opted in and some users are opted out of all Viva Insights surfaces.
* [Optional opt-in](#optional-opt-in). Some users have Viva Insights off by default and can opt themselves in later.

#### Default on

In this scenario, all surfaces of Viva Insights are turned on by default for all users. They will receive the welcome email and subsequent Viva digest emails and have access to the Viva Insights in Teams app, the Dashboard, the Viva Insights Outlook add-in, and inline suggestions in Outlook.

##### Confirm the configuration

>[!Note] 
> If you're a targeted release customer, you might see a new admin experience. To learn how confirm the configuration through this new experience, refer to [Using the new admin experience](../../advanced/setup-maint/new-admin-experience.md#personal-insights). 

**Role** - Microsoft 365 admin

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal). Make sure you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**. 
2. In the left pane, expand **Settings** and then select **Org settings**.
3. On the **Service** tab, select the option with **Microsoft Viva Insights** in it. This opens a page on which you can configure access to the different personal insights elements. It should show that all Viva Insights elements are enabled.
4. If any element is not enabled, select it to enable it and then select **Save changes**.
 
#### Default off

In this scenario, Viva Insights is off by default but users can turn it on for themselves &mdash; either all features at once or individual features. Users do not receive Viva digest emails but they can access their [Personal insights dashboard](https://myanalytics.microsoft.com/), where they can opt in to each surface individually.

##### Set Viva Insights off by default

**Role** - Microsoft 365 admin

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal). Make sure you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center.](../../images/mya/setup/the-new-admin-center.png)

2. In the left pane, expand **Settings** and then select **Org settings**.
3. On the **Service** tab, select **Microsoft Viva Insights**. This opens a page to configure access to Viva Insights elements.
4. Clear the selection for **Dashboard**, **Digest**, and **Viva Insights Outlook add-in** to keep all users in your organization opted out of all Viva Insights features.

After these settings are complete, users can open the dashboard and [turn on Viva Insights features by themselves](../use/opt-out-of-mya.md).

#### Mixed deployment

In this scenario, some users are opted in and some users are opted out of all Viva Insights surfaces. Those who are opted-in receive the digest emails, can open Viva Insights in Teams and the dashboard, and see the Viva Insights add-in in Outlook. Those who start out as opted out see the default “off” page shown here, where they can use Settings to opt in to any of the Viva Insights surfaces.

##### Set up mixed deployment

**Role** - Microsoft 365 admin

1. Turn off Viva Insights on all surfaces for all users. To do this, follow the steps in [Set Viva Insights off by default](#set-viva-insights-off-by-default).
2. Use the following steps to change access to Viva Insights for multiple users. Do this by running a PowerShell script that iterates through the users, changing the value one user at a time. (Also see [Exchange Online PowerShell V2 module](/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).)
3. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field of the users you want to configure. This will become your input .csv file. For example:

    ```
    UserPrincipalName
    ClaudeL@contoso.onmicrosoft.com
    LynneB@contoso.onmicrosoft.com
    ShawnM@contoso.onmicrosoft.com
    ```

4. Specify the location of the input .csv file, the output .csv file, and the value of PrivacyMode that you want to set for each user.
Note: The output.csv file will contain the results of running this PowerShell script. For more information about possible values for PrivacyMode, see Set-UserAnalyticsConfig / Parameters.

    ```powershell
    $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2License..csv>"
    $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2License-Done..csv>"
    $privacyMode = "Opt-in"
     
    $users=Import-Csv $inFileName
    ForEach ($user in $users)
    {
    $user.Userprincipalname
    $upn=$user.UserPrincipalName
    
    Set-UserAnalyticsConfig –Identity $upn -PrivacyMode $privacyMode
    Get-UserAnalyticsConfig –Identity $upn | Export-Csv $outFileName 
    }
    ```

5. Run the resulting commands at the Exchange Online PowerShell V2 module command prompt. For more information about the module, see [Exchange Online PowerShell V2 module](/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).

This PowerShell script does the following:

* Displays the user principal name for each user.
* Sets the specified privacy mode for each user.
* Creates a .csv file with all the users that were processed and shows their status.

#### Optional opt-in

In this scenario, some users have Viva Insights off by default and can opt themselves in; for some others, the service plan has been removed so they cannot opt in.

While Viva Insights is not available to these users, their data contributes to the email-read statistics for other users. For example, when they receive a qualifying email and read it, Viva Insights includes that statistic in the read percentage that's shown to the sender. A user can choose to not contribute data by turning the Viva Insights toggle off in the **Feature settings** pane of the Viva Insights dashboard.

##### To set up optional opt-in

This procedure is identical to [Set up mixed deployment](#set-up-mixed-deployment) with one important difference: Users are opted out to start with. In this procedure, the Microsoft 365 admin creates a .csv file that lists users who will start out as opted out but can choose to opt themselves in.

**Role** - Microsoft 365 admin

1. Follow steps 1 - 5 in [Set up mixed deployment](#set-up-mixed-deployment) and for step 4, use the following PowerShell command instead:

    ```powershell
    $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2License..csv>"
    $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2License-Done..csv>"
    $privacyMode = "Opt-out"
     
    $users=Import-Csv $inFileName
    ForEach ($user in $users)
    {
    $user.Userprincipalname
    $upn=$user.UserPrincipalName
    
    Set-UserAnalyticsConfig –Identity $upn -PrivacyMode $privacyMode
    Get-UserAnalyticsConfig –Identity $upn | Export-Csv $outFileName 
    }
    ```

   This PowerShell script does the following:

   * Displays the user principal name for each user.
   * Sets the specified privacy mode for each user.
   * Creates a .csv file with all the users that were processed and shows their status. 

   After you complete these steps, users can later use the dashboard to [opt themselves in](../use/opt-out-of-mya.md#if-i-opt-out-can-i-opt-back-in) if they so choose.

2. To ensure that particular users are not able to opt themselves into Viva Insights, remove the Viva Insights Service plan from those users.  

## Run a pilot rollout

For large organizations, we recommend that you run a small-scale pilot rollout before you deploy Viva Insights to the whole organization. This pilot can help you validate readiness and identify and mitigate any issues to help ensure a successful rollout. This section gives tips and describes the steps to run a pilot.

To get the most realistic results from the pilot, it should involve a group of actual users who are enthusiastic in trying new technologies and are willing to share their experiences with their colleagues.

### Pilot prerequisites

Before you start the pilot, have these in place:

* [Set and measure goals](#set-and-measure-goals). You’ll need clearly defined goals for measuring the success of the pilot.
* **Duration.** Identify the start and end dates of the pilot. Tip: Let it run for a minimum of 45 days.
* [Recruit pilot users](#recruit-pilot-users). Include a balanced mix of stakeholders and participants in the pilot group. Include a range of different roles, such as managers with direct reports and users from different departments.
* **Pace your work.** Start small and take time to pause, assess results, and adjust the pilot.

### Pilot timeline

We recommend that you follow these steps to conduct the pilot:

1. **Send a welcome email** - <!--(download [template](myanalytics-announcement-2020-template.docx))--> Send an email introducing Viva Insights to all the pilot users and invite them to training.
2. [Train the pilot participants](#train-pilot-participants) in how to use Viva Insights.
3. **Assign the service plan** - Before rolling out Viva Insights to the pilot users, ensure that all users have been assigned to a [Viva Insights service plan](../overview/plans-environments.md) in the Microsoft 365 admin center.
4. **Kick off the pilot** - Begin the pilot. Announce to the pilot participants that the pilot is starting and remind them of its duration and their tasks, as described in the [test plan](#design-a-test-plan). See [Conduct the pilot](#conduct-the-pilot) for more details.
5. **Consult with stakeholders** - Throughout the pilot, meet with your [project stakeholders](#include-stakeholders) to review user feedback as it arrives and address any technical issues that arise to ensure that the pilot is running smoothly.
6. **Assess and plan** - Use results from the pilot to plan your next steps. See [Assess the pilot lessons and make a plan](#assess-the-pilot-lessons-and-make-a-plan).

### Set and measure goals

To judge the success of the pilot, you need to know whether participants got value from the product and would recommend it to their colleagues. Consider using a survey to assess sentiment and usefulness of the product.

#### Design a test plan

For a successful pilot experience, give your participants clearly defined tasks to complete along with a way to share their feedback. Examples of what users can do in Viva Insights include:

* Opt in to one or all Viva Insights features.
* Automatically get focus time every day.
* Use the Insights tab to follow up with outstanding tasks, prepare for meetings, or follow up on unread documents.

#### Collect feedback

Ensure that you have an open feedback channel to track progress and measure outcomes, such as:

* Design a survey and use it after the pilot completes to capture and assess results. 
* Create a Teams channel or Yammer community for pilot participants to join and share their experiences. Alternatively, use Yammer.

### Recruit pilot users

The pilot users are part of the first phase of the company rollout. Communicate with them that are the first users of a new tool to drive personal productivity and improved work patterns at work. They should be willing to provide feedback. Share with them that their feedback will make things easier for all others in later phases of the rollout by helping to improve configuration knowledge, internal documentation, and notifications to participants. Note that it's best if the pilot users are not executive leaders.

Identifying pilot users might require discussion between the IT team and the department heads of target groups. In this discussion, try to identify users who are enthusiastic about using new tools to improve their work.

_Recommended:_ Consider grouping the pilot users into groups that correspond to the different [rollout scenarios](#rollout-scenarios). This lets the Microsoft 365 administrator get feedback about the different scenarios before implementing them at a larger scale.

### Train pilot participants

Your organization can choose an internal person responsible for training the pilot users. The trainer can use [Introduction to Microsoft Viva Insights](/training/modules/workplace-analytics-ways-working-action/) as a resource

### Conduct the pilot

The following is an example timeline for a 45-day pilot.

* **During the week before the pilot kickoff**:

  * Send initial communication to pilot users about what to expect and when. This is also a good opportunity to [conduct training](#train-pilot-participants) or share training materials about how to use Viva Insights. You can also send a survey now to compare user sentiment before and after the pilot.
  * Assign a Viva Insights service plan to pilot users in the Microsoft 365 admin center. Choose the rollout scenario and follow the admin rollout steps to enroll users into Viva Insights.

* **Day 1** – Send announcement email that the pilot is beginning.
* **Day 14** - Send a midpoint communication to the pilot users and optionally send a survey.
* **Day 40** – Send the final communication to the pilot users. Conduct a final survey on their experience.
* **Days 41–45** - Assess pilot results and plan for next steps.

### Assess the pilot lessons and make a plan

After the pilot is complete, gather all feedback surveys, support tickets, and other metrics. Analyze them with your goals in mind plan the actual Viva Insights rollout. Use your analysis of the pilot to decide whether your organization is ready for a broad deployment of Viva Insights. If it is not, consider extending the pilot to more users. See [Post-pilot options](#post-pilot-options).

#### Post-pilot options

| Were pilot goals achieved? | Consider these next steps |
| ----- | ----- |
| Yes (for example, user satisfaction was high) | You are ready to start the rollout phase. Depending on your goals, you can do one of the following: <ul> <li> Extend the pilot to additional participants, perhaps in different roles or with different collaboration patterns than the initial pilot group. </li> <li> Opt-in Viva Insights for other select groups in your organization. </li> <li> Opt-in Viva Insights for all other users in your organization. </li> </ul>  |
| No | Adjust your plan and revisit the pilot. To ensure that goals are achieved, we recommend that you tie the goals to existing initiatives within your organization. |

## Supporting documentation

If users have questions about using Viva Insights, point them to the published [Viva Insights FAQs](./../overview/mya-faq.md) for answers.

### Resources for stakeholders

<!--* Download the [Welcome Email template](/workplace-analytics/personal/setup/myanalytics-announcement-2020-template.docx). Edit and use this to communicate the availability of MyAnalytics as a productivity tool.-->

* [Privacy guide for Viva Insights admins](./../overview/privacy-guide-users.md). Use the Privacy guide to find answer to key questions about how Viva Insights processes information in a manner that protects employee privacy and supports compliance with local regulations.

* See these descriptions of the Viva Insights surfaces:

  * [Viva Insights app in Teams](../teams/viva-insights-home.md)
  * [Viva Insights Home page](./../use/home-web.md)
  * [Personal dashboard](./../use/dashboard-2.md)
  * [Viva Insights Outlook add-in](./../use/add-in.md)
  * [Briefing emails](../Briefing/be-overview.md)
  * [Digest emails](./../use/email-digests-3.md)
  * [Inline suggestions in Outlook](./../use/mya-notifications.md)

<!--#### Training videos for Viva Insights
These training Videos can be a great resource for people who will run a workshop to explain how to use Viva Insights.

##### Video: Viva Insights overview

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502351" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

##### Video: Viva Insights dashboard

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502493" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

##### Video: Outlook insights and inline suggestions

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502800" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>
-->
