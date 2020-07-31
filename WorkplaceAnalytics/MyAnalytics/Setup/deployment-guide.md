---

title: MyAnalytics deployment guide
description: Guide for admins on deploying MyAnalytics
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: mya

---

# Deploy MyAnalytics in your organization

MyAnalytics is an easy-to-deploy, out-of-the-box solution that helps users improve their productivity habits. It is available widely &mdash; to M365 users with [these Service plans](../overview/plans-environments.md). It is easy to deploy – after licenses are assigned, the MyAnalytics product is turned on by default, although you can customize your deployment by [following the steps in this guide](#roll-out-myanalytics). But before you deploy it, take a look at [What is MyAnalytics?](#what-is-myanalytics) for a brief description of benefits of using MyAnalytics in your organization.  

## What is MyAnalytics?
To quickly learn about MyAnalytics, watch [this video](https://www.youtube.com/watch?v=J9sokkEjGaE&feature=youtu.be):

[![What is MyAnalytics?](../../images/mya/setup/video-thumbnail.png)](https://www.youtube.com/watch?v=J9sokkEjGaE&feature=youtu.be)
_MyAnalytics -Personal Productivity Insights with Microsoft 365_

### Business value of MyAnalytics

More people than ever feel they lack control over their time at work. Many teams spend 80-90% of their week sitting in meetings, sending emails, and talking on the phone. But 50% of meeting time is seen to be unproductive and almost half of employees report that their work interferes with their family life.
MyAnalytics is an extension of your Microsoft 365 client experience that helps you find opportunities to build better habits and get back in control of your time. 

### Benefits of MyAnalytics 

By using MyAnalytics, you and your team can accomplish great things.

* **Improve work patterns through personal productivity insights:** MyAnalytics uses everyday data from Microsoft 365 to give you insights into how you spend your time and tips that help you work smarter.
* **Improve your relationships:** Increase your collaboration time, improve your team meetings, and grow your network.
* **Get more focus time:** Find more time to eliminate distractions, stop multi-tasking, and focus on your core priorities.
* **Improve your work-life balance:** Improve your work patterns and reduce the time you spend working for better work-life balance and overall wellbeing.

### Case studies

* Discover how a large Fortune 500 customer used MyAnalytics to foster wellbeing and productivity: [How Fannie Mae uses MyAnalytics](https://customers.microsoft.com/story/809849-fannie-mae-case-study-banking-microsoft-365)
   
   For employees who are new to remote work during the COVID-19 pandemic, having access to colleagues and information through Microsoft 365 tools at any time of day has been critical to staying productive, while MyAnalytics helps them use work hours more effectively. "Using the Focus scheduling feature is helping people block off time on their calendars each day to knock out priority projects, which is especially helpful for our employees who are juggling family needs along with work." _- Dawn Damico: Vice President of Digital Workplace, Fannie Mae_

* Hear how the world's largest brewer used MyAnalytics in conjunction with Workplace Analytics to change its workplace collaboration habits for the better: [ABInBev](https://customers.microsoft.com/story/758970-ab-inbev-consumer-goods-workplace-analytics) 
   
  [![ABInBev](../../images/mya/setup/ab-in-bev-video.png)](https://customers.microsoft.com/story/758970-ab-inbev-consumer-goods-workplace-analytics)

  _The use of MyAnalytics and Workplace Analytics at ABInBev_ 

## Roll out MyAnalytics 

You can deploy MyAnalytics in your organization all at once or in phases. In either case, before you roll out the product broadly, we recommend that you obtain additional buy-in, an optional step that is described in the following [preparatory steps](#preparatory-steps) section. 

### MyAnalytics rollout checklist

1.	(Optional) Complete the [preparatory steps](#preparatory-steps). 
2.	[Choose a rollout scenario](#choose-a-rollout-scenario). 
3.	Complete the steps in the rollout scenario that you chose. 

### Preparatory steps

It is easy to turn on MyAnalytics for all users in your organization as it comes with your [M365 subscription](./../overview/plans-environments.md). Here is a list of recommended but optional steps that your organization might consider: 

* **Create a communication plan:** Identify how your organization will effectively communicate with users during and after the rollout of MyAnalytics. Make it easy for users to find information about MyAnalytics. For example, use Yammer groups or SharePoint sites to help users learn about the benefits of using MyAnalytics within their organization.
* **Consider your stakeholders:** It may be important in your organization to identify and communicate with stakeholders ahead of rollout of MyAnalytics. Identify and inform them (you can use this five-minute [MyAnalytics overview video](#video-myanalytics-overview)). Also, see [Include stakeholders](#include-stakeholders). 
* **Consider running a pilot first:** Before scaling MyAnalytics to your entire organization, you might want to consider [running a pilot rollout](#run-a-pilot-rollout) with a subset of users. Especially for large organizations, it is a natural step to test a broad rollout on a small scale first by conducting a pilot to validate user readiness, identify and mitigate issues, and help ensure a successful organization-wide implementation. 
* **Security and Privacy:** MyAnalytics is secure and built to protect user privacy. The [Privacy guide](./../overview/privacy-guide.md) describes how MyAnalytics complies with privacy regulations. We recommended that you share this privacy guide with security and privacy teams to give them a better understanding of the privacy features of MyAnalytics.
* **Tie to existing initiative:** As you introduce MyAnalytics, tie it to an existing initiative or training plan within your organization such as an employee wellbeing initiative. Avoid introducing it as a technology tool but rather as a habit-changing tool that is integrated with the organization’s values. 

### Include stakeholders

Identifying and notifying your key stakeholders before the welcome email ([Download Welcome email template](https://docs.microsoft.com/workplace-analytics/myanalytics/setup/myanalytics-announcement-2020-template.docx)) is sent to users can be an important preliminary step in your rollout process. These stakeholders should understand the value, timelines, and expected experiences that come with the rollout of the Welcome email. When managed proactively, these stakeholders can become valuable advocates for moving the rollout process forward.

Here are some roles you might consider as part of the rollout project:

* **Executive sponsor.** Sends [welcome email](../use/mya-welcome-email.md) about the product, ideally with quotes about their experience with the product.
* **Security lead.** Reviews the [Privacy guide](../overview/privacy-guide.md) to learn about data security in MyAnalytics.
* **M365 admin.** Enables and disables MyAnalytics access per business requirements; see [Rollout scenarios](#rollout-scenarios). 
* **Support/Help-desk lead.** Manages questions from users. Some helpful answers can be found in the [MyAnalytics FAQs](./../overview/mya-faq.md).
* **Training lead.** Runs a training workshop. This person might find the [Training videos for MyAnalytics](#training-videos-for-myanalytics) helpful.

## Choose a rollout scenario

This section presents four scenarios for deploying MyAnalytics. An M365 admin can implement any of these scenarios either by using PowerShell or by using the Microsoft 365 Admin Center. Typically, admins use the Admin Center to broadly configure MyAnalytics for most or all users, and they use PowerShell to set specific configurations for select users.

### Rollout scenarios

Select and complete one of the following scenarios:

* [Default on](#default-on). For all users, all surfaces of MyAnalytics are turned on by default. This is the default scenario.
* [Default off](#default-off). MyAnalytics is off by default; users can individually turn on some or all MyAnalytics surfaces.
* [Mixed deployment](#mixed-deployment). Some users are opted in and some users are opted out of all MyAnalytics surfaces.
* [Optional opt-in](#optional-opt-in). Some users have MyAnalytics off by default and can opt themselves in later.

#### Default on

In this scenario, all surfaces of MyAnalytics are turned on by default for all users. They will receive the welcome email and the weekly email digest and they will have access to the MyAnalytics dashboard, the Insights add-in, and Outlook inline suggestions. 

##### Confirm the configuration 

**Role:** M365 Admin

1.	Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal). Make sure you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)
 
2.	In the left pane, expand **Settings** and then select **Org settings**.
3.	On the **Service** tab, select **MyAnalytics**. This opens a page on which you can configure access to MyAnalytics elements. It should show that all MyAnalytics elements are enabled. 
4. If any element is not enabled, select it to enable it and then select **Save changes**.
   
    ![Assign access](../../images/mya/setup/assign-mya-access-new.png)
 
#### Default off

In this scenario, MyAnalytics is off by default but users can turn it on for themselves &mdash; either all features at once or individual features. Users do not receive the email digest but they can access the MyAnalytics dashboard (at [myanalytics.microsoft.com](https://myanalytics.microsoft.com/)), where they can opt in to each surface individually. 

##### Set MyAnalytics to default off

**Role:** M365 Admin

1.	Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal). Make sure you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)
 
2.	In the left pane, expand **Settings** and then select **Org settings**.
3.	On the **Service** tab, select **MyAnalytics**. This opens a page to configure access to MyAnalytics elements.

    ![Assign access](../../images/mya/setup/assign-mya-access-new.png)

4.	Deselect **Insights dashboard**, **Weekly digest**, and **Insights Outlook add-in** to keep all MyAnalytics users in your organization opted out of all MyAnalytics features.

After these settings are complete, users can open the MyAnalytics dashboard and [turn on MyAnalytics features by themselves](https://docs.microsoft.com/workplace-analytics/myanalytics/use/opt-out-of-mya).

#### Mixed deployment 

In this scenario, some users are opted in and some users are opted out of all MyAnalytics surfaces. Those who are opted-in receive the weekly email digest, can open the MyAnalytics dashboard, and see the Outlook Insights add-in. Those who start out as opted out see the default “off” page shown here, on which they can use the Feature settings pane to opt in to any of the MyAnalytics surfaces:

![Feature settings](../../images/mya/setup/feature-settings.png)
_Feature settings pane with MyAnalytics off by default_ 

##### Set up mixed deployment

**Role:** M365 Admin

1.	Turn off MyAnalytics on all surfaces for all users. To do this, follow the steps in [Set MyAnalytics to default off](#set-myanalytics-to-default-off).
2.	Use the following steps to change access to MyAnalytics for multiple users. Do this by running a PowerShell script that iterates through the users, changing the value one user at a time. (Also see [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).) 
3.	Create a comma-separated value (.csv) text file that contains the UserPrincipalName field of the users you want to configure. This will become your input .csv file. For example:
   
    ```
    UserPrincipalName
    ClaudeL@contoso.onmicrosoft.com
    LynneB@contoso.onmicrosoft.com
    ShawnM@contoso.onmicrosoft.com
    ```

4.	Specify the location of the input .csv file, the output .csv file, and the value of PrivacyMode that you want to set for each user.
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

5.	Run the resulting commands at the Exchange Online PowerShell V2 module command prompt. For more information about the module, see [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).

This PowerShell script does the following:

* Displays the user principal name for each user.
* Sets the specified privacy mode for each user.
* Creates a .csv file with all the users that were processed and shows their status.

#### Optional opt-in

In this scenario, some users have MyAnalytics off by default and can opt themselves in; for some others, the service plan has been removed so they cannot opt in. 

Users without a service plan will see the following at [myanalytics.microsoft.com](https://myanalytics.microsoft.com/):

![No service plan](../../images/mya/setup/no-service-plan.png)
 
While MyAnalytics is not available to these users, their data contributes to the email-read statistics for other users. For example, when they receive a qualifying email and read it, MyAnalytics includes that statistic in the read percentage that's shown to the sender. A user can choose to not contribute data by turning the MyAnalytics toggle off in the **Feature settings** pane of the MyAnalytics dashboard.

##### To set up optional opt-in

This procedure is identical to [Set up mixed deployment](#set-up-mixed-deployment) with one important difference: Users are opted out to start with. In this procedure, the M365 admin creates a .csv file that lists users who will start out as opted out but can choose to opt themselves in. 

**Role:** M365 Admin

1. Follow steps 1 - 5 in [Set up mixed deployment](#set-up-mixed-deployment) with this exception: For step 4, use this PowerShell command: 

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
   
   After you complete these steps, users can later use the MyAnalytics dashboard to [opt themselves in](../use/opt-out-of-mya.md#if-i-opt-out-can-i-opt-back-in) if they so choose.

2.	To ensure that particular users are not able to opt themselves into MyAnalytics, remove the MyAnalytics Service plan from those users.  

## Run a pilot rollout

For large organizations, we recommend that you run a small-scale pilot rollout before you deploy MyAnalytics to the whole organization. This pilot can help you validate readiness and identify and mitigate any issues to help ensure a successful rollout. This section gives tips and describes the steps to run a pilot.

To get the most realistic results from the pilot, it should involve a group of actual users who are enthusiastic in trying new technologies and are willing to share their experiences with their colleagues.

### Pilot prerequisites

Before you start the pilot, have these in place:

* [Set and measure goals](#set-and-measure-goals). You’ll need clearly defined goals for measuring the success of the pilot. 
* **Duration.** Identify the start and end dates of the pilot. Tip: Let it run for a minimum of 45 days.
* [Recruit pilot users](#recruit-pilot-users). Include a balanced mix of stakeholders and participants in the pilot group. Include a range of different roles, such as managers with direct reports and users from different departments. 
* **Pace your work.** Start small and take time to pause, assess results, and adjust the pilot.

### Pilot timeline 

We recommend that you follow these steps to conduct the pilot:

1.	**Welcome email** (download [template](myanalytics-announcement-2020-template.docx)). Send this email to all pilot users and invite them to training.

2.	[Train the pilot participants](#train-pilot-participants) in how to use MyAnalytics. 

3.	**Assign the service plan.** Before rolling out MyAnalytics to the pilot users, ensure that all users have been assigned to a [MyAnalytics service plan](../overview/plans-environments.md) in the Microsoft 365 Admin Center. 

4.	**Kickoff.** Begin the pilot. Announce to the pilot participants that the pilot is starting and remind them of its duration and their tasks, as described in the [test plan](#design-a-test-plan). See [Conduct the pilot](#conduct-the-pilot) for more details.

5.	**Consult with stakeholders.** Throughout the pilot, meet with your [project stakeholders](#include-stakeholders) to review user feedback as it arrives and address any technical issues that arise to ensure that the pilot is running smoothly.

6.	**Assess and plan.** Use results from the pilot to plan your next steps. See [Assess the pilot lessons and make a plan](#assess-the-pilot-lessons-and-make-a-plan).

### Set and measure goals

To judge the success of the pilot, you need to know whether participants got value from the product and would recommend it to their colleagues. Consider using a survey to assess sentiment and usefulness of the product.

#### Design a test plan 

For a successful pilot experience, give your participants clearly defined tasks to complete along with a way to share their feedback. Examples of what users can do in MyAnalytics include:

* Opt in to one or all MyAnalytics features.
* Automatically get focus time every day. 
* Use the Insights tab to follow up with outstanding tasks, prepare for meetings, or follow up on unread documents.

#### Collect feedback

Ensure that you have an open feedback channel to track progress and measure outcomes, such as:

* Design a survey and use it after the pilot completes to capture and assess results. 
* Create a Teams channel or Yammer community for pilot participants to join and share their experiences. Alternatively, use Yammer.

### Recruit pilot users

The pilot users are part of the first phase of the company rollout. Communicate with them that are the first users of a new tool to drive personal productivity and improved work patterns at work. They should be willing to provide feedback; share with them that their feedback will make things easier for all others in later phases of the rollout by helping to improve configuration knowledge, internal documentation, and notifications to participants. Note that it's best if the pilot users are not executive leaders.

Identifying pilot users might require discussion between the IT team and the department heads of target groups. In this discussion, try to identify users who are enthusiastic about using new tools to improve their work.

_Recommended:_ Consider grouping the pilot users into groups that correspond to the different [rollout scenarios](#rollout-scenarios). This lets the M365 administrator get feedback about the different scenarios before implementing them at a larger scale. 

### Train pilot participants

Your organization can choose an internal person responsible for training the pilot users. The trainer can use [these videos](#training-videos-for-myanalytics) as training resources. 

### Conduct the pilot 

The following is an example timeline for a 45-day pilot:

* **During the week before the pilot kickoff** – 
  * Send initial communication to pilot users about what to expect and when. This is also a good opportunity to [conduct training](#train-pilot-participants) or share training materials about how to use MyAnalytics. You can also send a survey now to compare user sentiment before and after the pilot.
  * Assign a MyAnalytics service plan to pilot users in the Microsoft 365 Admin Center. Choose the rollout scenario and follow the admin rollout steps to enroll users into MyAnalytics.
* **Day 1** – Send announcement email that the pilot is beginning.
* **Day 14** - Send a midpoint communication to the pilot users and optionally send a survey.
* **Day 40** – Send the final communication to the pilot users. Conduct a final survey on their experience.
* **Days 41–45** - Assess pilot results and plan for next steps.

### Assess the pilot lessons and make a plan

After the pilot is complete, gather all feedback surveys, support tickets, and other metrics. Analyze them with your goals in mind plan the actual MyAnalytics rollout. Use your analysis of the pilot to decide whether your organization is ready for a broad deployment of MyAnalytics. If it is not, consider extending the pilot to more users. See [Post-pilot options](#post-pilot-options). 

#### Post-pilot options

| Were pilot goals achieved? | Consider these next steps |
| ----- | ----- |
| Yes (for example, user satisfaction was high) | You are ready to start the rollout phase. Depending on your goals, you can do one of the following: <ul> <li> Extend the pilot to additional participants, perhaps in different roles or with different collaboration patterns than the initial pilot group. </li> <li> Opt-in MyAnalytics for other select groups in your organization. </li> <li> Opt-in MyAnalytics for all other users in your organization. </li> </ul>  |
| No | Adjust your plan and revisit the pilot. To ensure that goals are achieved, we recommend that you tie the goals to existing initiatives within your organization. |

## Supporting documentation 

If users have questions about using MyAnalytics, point them to the published [MyAnalytics FAQs](./../overview/mya-faq.md) for answers. 

### Resources for stakeholders 

* Download the [Welcome Email template](https://docs.microsoft.com/workplace-analytics/myanalytics/setup/myanalytics-announcement-2020-template.docx). Edit and use this to communicate the availability of MyAnalytics as a productivity tool.

* [Privacy guide for MyAnalytics admins](./../overview/privacy-guide.md). Use the Privacy guide to find answer to key questions about how MyAnalytics processes information in a manner that protects employee privacy and supports compliance with local regulations.

* See these descriptions of the MyAnalytics surfaces:

  * [Personal dashboard](./../use/dashboard-2.md)
  * [Insights Outlook add-in](./../use/add-in.md)
  * [Weekly digest](./../use/email-digest-2.md)
  * [Inline suggestions in Outlook](./../use/mya-notifications.md)


#### Training videos for MyAnalytics
These training Videos can be a great resource for people who will run a workshop to explain how to use MyAnalytics.

##### Video: MyAnalytics overview

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502351" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

##### Video: MyAnalytics dashboard

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502493" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

##### Video: Outlook insights and inline suggestions

<iframe width="580" height="512" src="https://player.vimeo.com/video/440502800" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>



