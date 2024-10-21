---

ms.date: 05/13/2020
title: Conduct a user pilot
description: Helps you conduct a pilot rollout for the Briefing email
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.service: viva-insights
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: helayne

---

# Conduct a user pilot

>[!Important]
>We've paused sending Briefing emails to make some improvements. Users can still access the [Viva Insights Outlook add-in](../use/add-in.md) or [Viva Insights app in Teams](../teams/introduction.md) for key functionality until this service resumes. For more information about this change, refer to [Briefing pause](../reference/briefing-pause.md).

If you choose to disable the Briefing email for your organization, you can run a pilot with a subset of users first. Especially for large organizations, a small-scale pilot is a natural first step to validate user readiness, identify and mitigate issues, and help ensure a successful, organization-wide rollout.

To achieve the most realistic results, the pilot should involve a group of actual users, mimic how they regularly communicate and collaborate, and verify both technical and user experiences.  

## Outline pilot logistics

A successful pilot includes the following:

* Defined start and end dates and clearly defined goals for measuring success. These goals can help you plan the rollout after the pilot is complete.  
* Allow enough time to run the pilot and assess its impact, which a minimum of 30 days is recommended.  
* Include the right stakeholders and participants, knowing you can add more users throughout the pilot, if necessary.  
* Start small and take time to pause, assess results, and adjust the pilot.  

## Recruit pilot participants

The most important task when planning a pilot is thoughtfully selecting the participants. Today, the Briefing email shows insights, such as tasks identified in email and documents related to upcoming meetings. The best participants for your pilot are people who have consistent email and calendar activity because they would regularly get the Briefing email and can benefit the most by using it for daily work activities.

A great place to start is to ask your stakeholders and department managers which teams they think would benefit from the assistance offered in the Briefing email. The pilot should also extend to key people in IT, Training, Corporate communications, and your Help desk. This allows for those in key roles in your organization to have an opportunity to familiarize themselves with the capabilities of the Briefing email.

>[!Tip]
>When selecting a group of people for your Briefing pilot, be sure to include those who check email on Adaptive-compatible clients. The [Adaptive version](be-overview.md#adaptive-or-html-version) ensures users get the optimal experience with links to open tasks, upcoming meetings, related documents, and book suggested focus time, all within the email.

You can control who receives the Briefing email in your pilot in one of the following ways:

* Use the admin center to set the default state for all people in your organization as opted out. Then advise your pilot participants to [opt in](be-settings.md#change-your-settings) to receive the Briefing email in their Viva Insights app in Teams or on the web.
* Use PowerShell to disable Briefing for non-pilot users and leave pilot users enabled. In the admin center, have all users opted-in by default.

  * Users who are enabled and opted-in will receive the Briefing email.
  * Users who are disabled and opted-in will not receive the Briefing email. Note that as you onboard new users to a tenant, you will need to use PowerShell to disable Briefing for them if you do not want them to be part of the pilot.

## Design your test plan and feedback survey

For a successful pilot experience, give your participants clearly defined tasks to complete along with a way to share their feedback. Examples of what users can do in the Briefing email include:

* Organize or accept a meeting invite with a cloud document attached (can be a link in the invite itself, a reply to the original invite, or sent in a related email thread).
* When documents appear in the Briefing email, they can open them directly from the email and mark them as **Done** or **Not related**.
* Review tasks identified by opening the linked source email and marking the tasks as Done or Not a task.
* Book focus time where available in your calendar.

Ensure you have an open feedback channel to track progress and measure outcomes, such as:

* Use a predefined survey as an easy way to capture and assess pilot results. You can use the [Sample feedback surveys](https://download.microsoft.com/download/a/9/f/a9fea3f4-77a9-4465-a6eb-c021087c3b7f/feedback-survey.docx) to get started.
* Create a Team or Channel for pilot participants to join and share their experiences.
* Create a Security group where pilot users can ask questions and submit feedback.

## Create your communications plan

It's crucial to the success of your pilot that you educate pilot participants on what's happening when and why, and what's expected of them. To drive excitement and maximum participation, be sure you include value messaging and links to Training and Support where users can get additional information throughout the pilot. The following resources are available to get you started with a pilot communications plan:

* [One-page Briefing overview](https://download.microsoft.com/download/6/6/f/66fa5ad1-ee36-48f2-a01a-06fb918b278c/briefing-overview.docx)
* [Sample email introducing the Briefing email](https://download.microsoft.com/download/6/4/9/649c7338-4cfe-45fe-b9bd-34ba4e0fa249/email-to-introduce-briefing.docx)
* [Demo for the Adaptive version of the Briefing email](briefing-demo.gif)

## Pilot planning tips

The following tips can help ensure the success of your pilot:

* Remember the Briefing email is enabled by default for everyone with an Exchange Online mailbox in a [supported language](be-languages.md). You can use [PowerShell](be-admin.md) to choose who gets the Briefing email first.
* Before beginning a pilot, confirm that all pilot participants have active Exchange Online licenses.
* Throughout a pilot, meet with your project stakeholders to review user feedback and help desk tickets to ensure the pilot is running smoothly. Make any adjustments as necessary.

The following is an example timeline for a 30-day pilot:

* **One week before the pilot kickoff** - Send initial communication to pilot users about what to expect and when. This is also a good opportunity to conduct training or share training materials about how to use the Briefing email. You can also send a survey now to compare user sentiment before and after the pilot.
* **Day 1** - Send kickoff communication to pilot users.
* **Day 14** - Send midpoint communication to pilot users and optionally send a survey.
* **Day 30** - Send final communication to pilot users. Conduct a final survey on their experience.
* **Days 31–45** - Assess pilot results and plan for next steps.

## Assess learnings and make a plan

After a pilot is complete, gather all of the feedback surveys, support tickets, and other metrics to analyze with your goals and decide your plan for the rollout. Your analysis should help you decide if your organization is ready for a broad deployment of Briefing, or if you need to extend the pilot to more users, or revisit the pilot after you've identified and mitigated any concerns.

When the results indicate:

* **The pilot goals were achieved** (for example, user satisfaction)– You are ready to start the rollout phase. Depending on your goals, you can do one of the following:

  * Extend the pilot to additional participants, perhaps in different roles or with different collaboration patterns than the initial pilot group.
  * Enable Briefing for other select groups in your organization.
  * Enable Briefing for all other users in your organization.

* **The pilot didn't achieve the goals** - Take some time to make adjustments to your plan and revisit the pilot.

 > [!Tip]
 > Enlist your pilot participants as peer champions to help evangelize and onboard new users to Briefing. Peer champions can easily relate to other users, sharing their own experiences and learnings, and offering support and guidance to their colleagues.

