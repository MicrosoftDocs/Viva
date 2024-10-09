---

ms.date: 10/09/2024
title: Personal insights deployment guide
description: Guide for admins on deploying personal insights with Microsoft Viva Insights
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.service: viva-insights
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: helayne
audience: Admin

---

# Personal insights deployment guide

As an administrator, you benefit from knowing what Microsoft Viva Insights provides to its participants and what you can do to enable and enhance their experience.

## What is Viva Insights?

To quickly learn about Viva Insights, check out [Microsoft Viva Insights](https://www.microsoft.com/microsoft-viva/insights).

## Benefits of use

Viva Insights can help participants strengthen their work relationships, have more time to focus on important work, and improve their work-life balance. Viva Insights does this by showing users insights about their work habits. It derives these insights from Microsoft 365 data about emails, meetings, calls, and chats. 

By using Viva Insights, you and your team can accomplish great things.

* **Improve work patterns through personal productivity insights** – Viva Insights uses everyday data from Microsoft 365 to give you insights into how you spend your time and tips that help you work smarter.
* **Improve your relationships** – Increase your collaboration time, improve your team meetings, and grow your network.
* **Get more focus time** – Find more time to eliminate distractions, stop multi-tasking, and focus on your core priorities.
* **Improve your work-life balance** – Improve your work patterns and reduce the time you spend working for better work-life balance and overall wellbeing.

### Business value of Viva Insights

More people than ever feel they lack control over their time at work. Many teams spend 80-90% of their week sitting in meetings, sending emails, and talking on the phone. But 50% of meeting time is seen to be unproductive and almost half of employees report that their work interferes with their family life.

Viva Insights is an extension of your Microsoft 365 client experience that helps you find opportunities to build better habits and get back in control of your time.

## You and your users are in charge

* As the admin, you control the configuration of how your users start using Viva Insights. See [Configure personal insights](../../advanced/setup-maint/configure-personal-insights.md) for details.
* Users can opt in or out from the start, including for the [app](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f), [digest emails](https://support.microsoft.com/topic/digest-email-0e8b9a77-d1ce-4139-82bc-e91a3cb909c3), [inline suggestions](https://support.microsoft.com/topic/inline-suggestions-in-outlook-064a323e-6dc7-40e9-ab1b-199de8d39db5), and the [Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d). See [Opt out](https://support.microsoft.com/topic/opt-out-of-viva-insights-ecfd76f9-52ef-4882-9235-be1f59c25967) for details.


## Data privacy

None of a user's personal information is shared with their co-workers or managers. Viva Insights adheres to compliance regulations, such as the GDPR. Also see the [Privacy guide for admins](../overview/privacy-guide-admins.md).

## Granting access

Soon after you assign licenses with a Microsoft Viva Insights service plan to users, they'll get access to personal insights elements, such as [Viva Insights in Teams and on the web](../teams/introduction.md), [digest emails](../use/email-digests-3.md), [inline suggestions in Outlook](../use/mya-notifications.md), the [Viva Insights Outlook add-in](../use/add-in.md), and a [Viva Insights welcome message](../use/mya-welcome-email.md).

Access to these elements depends on the plan in place at your organization. For details, see [Access to Viva Insights elements](../../advanced/setup-maint/environment-requirements.md#access-to-viva-insights-elements).

Personal insights with Microsoft Viva Insights is an easy-to-deploy, out-of-the-box solution that helps you and your co-workers improve your personal productivity habits. It is available widely &mdash; to Microsoft 365 users with [these service plans](../../advanced/setup-maint/environment-requirements.md#microsoft-365-plans). After licenses are assigned, the Viva Insights is turned **On** by default, although you can customize your deployment by [following the steps in this guide](#roll-out-viva-insights).

## Roll out Viva Insights 

You can deploy Viva Insights in your organization all at once or in phases. In either case, before you roll out the product broadly, we recommend that you obtain additional buy-in, an optional step that is described in the following [preparatory steps](#preparatory-steps) section.

### Viva Insights rollout checklist

1. (Optional) Complete the [preparatory steps](#preparatory-steps).
2. [Choose a rollout scenario](#choose-a-rollout-scenario).
3. Complete the steps in the rollout scenario that you chose.

### Preparatory steps

It's easy to turn on Viva Insights for all users in your organization, because it comes with your [Microsoft 365 subscription](../../advanced/setup-maint/environment-requirements.md). Here's a list of recommended, but optional, steps that your organization might consider before turning on Viva Insights:

* **Create a communication plan** – Identify how your organization will effectively communicate with users during and after the rollout of Viva Insights. Make it easy for users to find information about Viva Insights. For example, use Viva Engage groups or SharePoint sites to help users learn about the benefits of using Viva Insights within their organization.
* **Consider your stakeholders** – It may be important in your organization to identify and communicate with stakeholders ahead of rollout of Viva Insights. See [Include stakeholders](#include-stakeholders). 
* **Consider running a pilot first** – Before scaling Viva Insights to your entire organization, you might want to consider [running a pilot rollout](#run-a-pilot-rollout) with a subset of users. Especially for large organizations, it is a natural step to test a broad rollout on a small scale first by conducting a pilot to validate user readiness, identify and mitigate issues, and help ensure a successful organization-wide implementation. 
* **Security and Privacy** – Viva Insights is secure and built to protect user privacy. The [Privacy guide](../overview/privacy-guide-admins.md) describes how Viva Insights complies with privacy regulations. We recommended that you share this privacy guide with security and privacy teams to give them a better understanding of the privacy features of Viva Insights.
* **Tie to existing initiative** – As you introduce Viva Insights, tie it to an existing initiative or training plan within your organization such as an employee wellbeing initiative. Avoid introducing it as a technology tool but rather as a habit-changing tool that is integrated with the organization’s values. 

### Include stakeholders

Identifying and notifying your key stakeholders before the welcome email is sent to users can be an important preliminary step in your rollout process. These stakeholders should understand the value, timelines, and expected experiences that come with the rollout of the Welcome email. When managed proactively, these stakeholders can become valuable advocates for moving the rollout process forward. 

Here are some roles you might consider as part of the rollout project:

* **Executive sponsor** Send welcome email about Viva Insights, ideally with quotes about their experience with the product.
* **Security lead** – Reviews the [Privacy guide](../overview/privacy-guide-admins.md) to learn about data security in Viva Insights.
* **Microsoft 365 admin** – Enables and disables Viva Insights access per business requirements; see [Rollout scenarios](#rollout-scenarios). 
* **Support or Help desk lead** – Manages questions from users. Some helpful answers can be found in the [personal insights FAQs](./../overview/mya-faq.md).
* **Training lead** – Runs a training workshop about Viva Insights.

## Choose a rollout scenario

This section presents four scenarios for deploying Viva Insights. A Microsoft 365 admin can implement any of these scenarios either by using PowerShell or by using the Microsoft 365 admin center. Typically, admins use the admin center to broadly configure Viva Insights for most or all users, and they use PowerShell to set specific configurations for select users.

### Rollout scenarios

Select and complete one of the following scenarios:

* [Default on](#default-on). For all users, all surfaces of Viva Insights are turned on by default. This is the default scenario.
* [Default off](#default-off). Viva Insights is off by default; users can individually turn on some or all Viva Insights surfaces.
* [Mixed deployment](#mixed-deployment). Some users are opted in and some users are opted out of all Viva Insights surfaces.

#### Default on

In this scenario, all surfaces of Viva Insights are turned on by default for all users. They'll receive the welcome email and subsequent Viva digest emails and have access to the Viva Insights app on the web, the Viva Insights Outlook add-in, and inline suggestions in Outlook.

Learn how to implement this rollout scenario in [Configure personal insights defaults](../../advanced/setup-maint/configure-personal-insights.md#to-enable-access-to-viva-insights-features).

#### Default off

In this scenario, Viva Insights is off by default but users can turn it on for themselves &mdash; either all features at once or individual features. Users do not receive Viva digest emails but they can opt in to each surface individually through their Viva Insights app in Teams or on the web.

Learn how to implement this rollout scenario in [Configure personal insights defaults](../../advanced/setup-maint/configure-personal-insights.md#to-enable-access-to-viva-insights-features)

#### Mixed deployment

In this scenario, some users are opted in and some users are opted out of all Viva Insights surfaces. Those who are opted-in receive the digest emails, can open Viva Insights in Teams and the web, and see the Viva Insights add-in in Outlook. Those who start out as opted out see the default “off” page shown here, where they can use Settings to opt in to any of the Viva Insights surfaces.

Learn how to implement this rollout scenario in [Configure personal insights defaults](../../advanced/setup-maint/configure-personal-insights.md#enable-or-disable-features-1).

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

1. **Send a welcome email** – Send an email introducing Viva Insights to all the pilot users and invite them to training.
2. [Train the pilot participants](#train-pilot-participants) in how to use Viva Insights.
3. **Assign the service plan** – Before rolling out Viva Insights to the pilot users, ensure that all users have been assigned to a [Viva Insights service plan](../overview/plans-environments.md) in the Microsoft 365 admin center.
4. **Kick off the pilot** – Begin the pilot. Announce to the pilot participants that the pilot is starting and remind them of its duration and their tasks, as described in the [test plan](#design-a-test-plan). See [Conduct the pilot](#conduct-the-pilot) for more details.
5. **Consult with stakeholders** – Throughout the pilot, meet with your [project stakeholders](#include-stakeholders) to review user feedback as it arrives and address any technical issues that arise to ensure that the pilot is running smoothly.
6. **Assess and plan** – Use results from the pilot to plan your next steps. See [Assess the pilot lessons and make a plan](#assess-the-pilot-lessons-and-make-a-plan).

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
* Create a Teams channel or Viva Engage community for pilot participants to join and share their experiences. Alternatively, use Viva Engage.

### Recruit pilot users

The pilot users are part of the first phase of the company rollout. Communicate with them that are the first users of a new tool to drive personal productivity and improved work patterns at work. They should be willing to provide feedback. Share with them that their feedback will make things easier for all others in later phases of the rollout by helping to improve configuration knowledge, internal documentation, and notifications to participants. Note that it's best if the pilot users are not executive leaders.

Identifying pilot users might require discussion between the IT team and the department heads of target groups. In this discussion, try to identify users who are enthusiastic about using new tools to improve their work.

_Recommended:_ Consider grouping the pilot users into groups that correspond to the different [rollout scenarios](#rollout-scenarios). This lets the Microsoft 365 administrator get feedback about the different scenarios before implementing them at a larger scale.

### Train pilot participants

Your organization can choose an internal person responsible for training the pilot users. 

### Conduct the pilot

The following is an example timeline for a 45-day pilot.

* **During the week before the pilot kickoff**:

  * Send initial communication to pilot users about what to expect and when. This is also a good opportunity to [conduct training](#train-pilot-participants) or share training materials about how to use Viva Insights. You can also send a survey now to compare user sentiment before and after the pilot.
  * Assign a Viva Insights service plan to pilot users in the Microsoft 365 admin center. Choose the rollout scenario and follow the admin rollout steps to enroll users into Viva Insights.

* **Day 1** – Send announcement email that the pilot is beginning.
* **Day 14** – Send a midpoint communication to the pilot users and optionally send a survey.
* **Day 40** – Send the final communication to the pilot users. Conduct a final survey on their experience.
* **Days 41–45** – Assess pilot results and plan for next steps.

### Assess the pilot lessons and make a plan

After the pilot is complete, gather all feedback surveys, support tickets, and other metrics. Analyze them with your goals in mind plan the actual Viva Insights rollout. Use your analysis of the pilot to decide whether your organization is ready for a broad deployment of Viva Insights. If it is not, consider extending the pilot to more users. See [Post-pilot options](#post-pilot-options).

#### Post-pilot options

| Were pilot goals achieved? | Consider these next steps |
| ----- | ----- |
| Yes (for example, user satisfaction was high) | You are ready to start the rollout phase. Depending on your goals, you can do one of the following: <ul> <li> Extend the pilot to additional participants, perhaps in different roles or with different collaboration patterns than the initial pilot group. </li> <li> Opt-in Viva Insights for other select groups in your organization. </li> <li> Opt-in Viva Insights for all other users in your organization. </li> </ul>  |
| No | Adjust your plan and revisit the pilot. To ensure that goals are achieved, we recommend that you tie the goals to existing initiatives within your organization. |

## Supporting documentation

If users have questions about using Viva Insights, point them to the [personal insights FAQs](./../overview/mya-faq.md) for answers.

### Resources for stakeholders

* [Privacy guide for Viva Insights admins](../overview/privacy-guide-admins.md). Use the Privacy guide to find answer to key questions about how Viva Insights processes information in a manner that protects employee privacy and supports compliance with local regulations.

* See these descriptions of the Viva Insights surfaces:

  * [Viva Insights app in Teams](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f)
  * [Viva Insights Home page](https://support.microsoft.com/topic/viva-insights-home-tab-6e7d28b2-6b0e-4367-9b52-1999a86eb391)
  * [Viva Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d)
  * [Inline suggestions in Outlook](https://support.microsoft.com/topic/inline-suggestions-in-outlook-064a323e-6dc7-40e9-ab1b-199de8d39db5)



