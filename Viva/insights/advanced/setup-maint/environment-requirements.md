---

ms.date: 03/19/2024
title: Environment requirements for Viva Insights
description: Describes the environment requirements for using Microsoft Viva Insights
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: 
- m365initiative-viva-insights
- essentials-manage
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Environment requirements for Viva Insights

Environment requirements vary depending on the type of insights you view in Microsoft Viva Insights. The types of insights are: personal insights, manager insights or leader insights in Microsoft Teams, and advanced insights in the web-based service.

## Personal insights

Microsoft Viva Insights provides personal insights in the [Viva Insights app in Teams and on the web](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f), [Briefing emails](../../personal/Briefing/be-overview.md), [Viva digest emails](https://support.microsoft.com/topic/digest-email-0e8b9a77-d1ce-4139-82bc-e91a3cb909c3), [Viva Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d), and [inline suggestions](https://support.microsoft.com/topic/inline-suggestions-in-outlook-064a323e-6dc7-40e9-ab1b-199de8d39db5).

>[!Important]
>Beginning at the end of March 2024, we’ll be pausing the Digest email, which is typically sent twice a month. All the content from Digest emails will still be available within the [Viva Insights app in Teams or on the web.](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f) You can continue to explore and analyze your data insights seamlessly. To learn more about this change, refer to the [Digest email pause.](/Viva/insights/personal/reference/digest-pause)

  >[!Important]
  >We've paused sending Briefing emails to make some improvements. You can still access the [Viva Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d) or [Viva Insights app in Teams](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f) for key functionality until this service resumes. For more information about this change, refer to [Briefing pause](../../personal/reference/briefing-pause.md).

### Microsoft 365 plans

The following Personal insights service plans are generally available with a subscription to the Microsoft 365 plans listed for each. Also see [Supported](#supported-microsoft-365-environments) and [Not supported](#not-supported-microsoft-365-environments) Microsoft 365 environments to confirm your type of environment is supported.

* With the following Microsoft 365 plans, a [**Viva Insights subscription**](https://www.microsoft.com/microsoft-viva/buy-insights) is available for purchase:

  * Microsoft 365 E3, A3, E5, A5, Business Basic, Business Standard, or Business Premium
  * Office 365 E1, E3, A3, E5, A5
  * Exchange Online Plan 1 or 2

* **MyAnalytics (Full)** and **Insights by MyAnalytics** service plans are included with:

  * Microsoft 365 E5 (with or without Audio Conferencing) or G5
  * Office 365 Enterprise, G5, or Nonprofit E5

* **MyAnalytics (Full)** service plan is included with:

  * Microsoft 365 A5 for faculty and students
  * Office 365 A5 for faculty and students

* **Insights by MyAnalytics** service plan is included with:

  * Microsoft 365 E3, Business, or A3 for faculty and students
  * Office 365 E1, E3, A3 for faculty and students, E3 Developer, G1, G3, Business Premium, or Business Essentials

#### Supported Microsoft 365 environments

* Worldwide Multi-tenant
* Dedicated Multi-tenant
* Government Community Cloud (GCC)
* GCC-High
* Department of Defense (DoD)

>[!Note]
>For more information about the features available and unavailable in GCC-High and DoD environments, refer to the [Microsoft Viva service description](/office365/servicedescriptions/microsoft-viva-service-description).

#### Not supported Microsoft 365 environments

* Microsoft 365 Germany
* Microsoft 365 Operated by 21Vianet

>[!Note]
>
>* To determine what your plan and service plan are, see [How do I find my plan?](../../personal/overview/mya-faq.md#q2-how-can-i-find-out-what-my-plan-is).
>* For more information about the plans that offer these user experiences, see [Microsoft 365 business plans](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans).

### Access to Viva Insights elements

After users get assigned licenses with an applicable service plan, they get access to the following within the specified time frames.

| Element | Approximate time frame |
| ------- | ------------------|
| Welcome email | Sent to existing Microsoft 365 users a few days (up to four weeks) after license assignment; sent to new users approximately four weeks after license assignment |
| [Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d) and [Inline suggestions](https://support.microsoft.com/topic/inline-suggestions-in-outlook-064a323e-6dc7-40e9-ab1b-199de8d39db5) | Available about one day after license assignment |
|[Viva Insights in Teams and on the web](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f) | Available a few days after license assignment |
| [Digest emails](https://support.microsoft.com/topic/digest-email-0e8b9a77-d1ce-4139-82bc-e91a3cb909c3) | Sent two to three weeks after the welcome email |

>[!Note]  
>
>* _Licensed users_ have the personal insights features with Viva Insights automatically enabled after license assignment.
>* _All users_ in your organization are opted-in, whether or not they have licenses with a Viva Insights subscription. If you want one or more licensed users to be opted _out_ by default, see [Set access for one user](../../advanced/setup-maint/configure-personal-insights.md#set-access-for-one-user) and [Set access for multiple users](../../advanced/setup-maint/configure-personal-insights.md#set-access-for-multiple-users).

### Other features and eligibility requirements

| Feature/card | Requirement |
| ------- | ------------------|
| [Schedule send suggestions in chat](https://support.microsoft.com/topic/schedule-send-suggestions-in-teams-chat-6f9a22b6-b269-4264-93f2-55b5254d3c62) | [Viva Insights subscription](https://www.microsoft.com/microsoft-viva/insights)  |
| [Shorten a meeting and Track email open rate (inline suggestion)](https://support.microsoft.com/topic/inline-suggestions-in-outlook-064a323e-6dc7-40e9-ab1b-199de8d39db5)  | Viva Insights subscription  |
| [Meeting category insights](https://support.microsoft.com/topic/meeting-category-insights-in-viva-insights-17962415-0c3a-4931-9aa8-3191a7b6337a)  | Viva Insights subscription  |
| [Meeting effectiveness surveys](https://support.microsoft.com/topic/meeting-effectiveness-surveys-in-viva-insights-2eb63cc8-a6a1-4ab8-b643-80da6562aa22) | Viva Insights subscription  |
| [Shared meeting plan (organizer)](https://support.microsoft.com/topic/shared-meeting-plan-in-viva-insights-30c3d08b-5761-4ff7-ba7d-32d9f00759a4) | Viva Insights subscription  |
| [Shared no-meeting day plan](https://support.microsoft.com/topic/shared-no-meeting-day-plan-32d22a61-280f-487d-b352-47effe338fbb)  | Viva Insights subscription  |
| [Shared focus plan](https://support.microsoft.com/topic/shared-focus-plan-6847226d-e5b1-498a-a7a5-e77d4405bb97) | Viva Insights subscription  |
| [Schedule breaks, learning, and message catch-up](https://support.microsoft.com/topic/time-management-features-in-viva-insights-da568337-8568-47cd-9f47-213537873571)  | Viva Insights subscription  |
| [Schedule send suggestions in email](https://support.microsoft.com/topic/schedule-send-in-outlook-0b0c0c20-8fa1-44b9-b5bc-57f160046639)  | MyAnalytics (Full) service plan |
| [Quiet time](https://support.microsoft.com/topic/quiet-time-in-viva-insights-ec70888d-8840-4f20-9819-af6bfc17e143) | Insights by MyAnalytics  |
| [Focus plan](https://support.microsoft.com/topic/focus-plan-for-viva-insights-a079a744-010e-4fee-8552-a2799d0c62ea) | Insights by MyAnalytics |
| [Send praise](https://support.microsoft.com/topic/praise-in-viva-insights-4977c923-f3d1-4134-9d1c-ee29dc01ae27) | Insights by MyAnalytics  |
| [Virtual commute](https://support.microsoft.com/topic/virtual-commute-in-viva-insights-8be83785-f5ec-4e84-8cff-f0abb117f876) | Insights by MyAnalytics  |
| [Headspace](https://support.microsoft.com/topic/mindfulness-content-in-viva-insights-c5c807e1-b10c-4d41-9120-b2ac914dcc72) | Insights by MyAnalytics  |
| [Breather break](https://support.microsoft.com/topic/quiet-time-in-viva-insights-ec70888d-8840-4f20-9819-af6bfc17e143) | Insights by MyAnalytics  |
| [Reflect](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743) | Insights by MyAnalytics  |

The table above isn't a complete list of Viva Insights features. Other cards might appear depending on your type of plan.

### Browser support

You can use the following web browsers to view all web-based personal insights features.

* Microsoft Edge or Edge Chromium (coming soon)
* Microsoft Internet Explorer version 10 or 11
* Google Chrome (latest version)
* Apple Safari (latest version)
* Mozilla Firefox (latest version)

As an Outlook add-in, the Insights Outlook add-in requires a browser compatible with your system's platform and operating system. For details, see [Browsers used by Microsoft 365 add-ins](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins).

### Language support

Personal insights in Viva Insights are available in most of the same languages as Microsoft 365. See [What languages is Office available in](https://support.office.com/article/what-languages-is-office-available-in-26d30382-9fba-45dd-bf55-02ab03e2a7ec).

See [Briefing languages](../../personal/briefing/be-languages.md) to see what's supported for Briefing emails and [Advanced insights language support](../../overview/supported-languages.md) for what's supported for advanced insights.

### Prerequisite and exclusion

* **Prerequisite**: [Microsoft Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-service-description) is required. 

  > [!Note]
  > Also refer to **Prerequisites to access the Viva Insights Outlook add in** in [About the Viva Insights Outlook add-in](https://support.microsoft.com/topic/about-the-viva-insights-outlook-add-in-48b73ccf-4086-4f13-9f62-dcee91a9df6d).

* **Licensing exclusion**: Shared mailboxes aren't supported.

## Manager, leader, and advanced insights

With the applicable [Viva Insights licensing](#viva-insights-licenses), your company can get manager and leader insights in Teams, and advanced insights features as an add-on to the licensing agreement.

Microsoft Exchange Online provides much of the collaboration data that Viva Insights uses. For this reason, we recommend you have a Microsoft 365 or an Office 365 product that contains Exchange Online Plan 1 and Plan 2.

## Channel support

Other channels such as Cloud Solution Provider (CSP) don't support the addition of Viva Insights at this time. Also, note the following circumstances for various types of customers:

|  Type  | Notes |  
|---- | ---- |
|Government | Government Community Cloud (GCC) supports personal insights only. |
|Education | Supported only for the analysis of faculty at this time, not for students. |
|Commercial | You can add Viva Insights with commercial enrollments. |
|Non-profit | Viva Insights can be used by nonprofits but non-profit pricing isn't available. |
|First-line workers | Viva Insights doesn't support analysis of first-line workers that use Microsoft Firstline Worker SKUs (F1, F3, F5) at this time. |

## Tenant environments

Viva Insights requires the applicable [Viva Insights licensing](#viva-insights-licenses) and a Microsoft 365 or Office 365 tenant with Exchange Online Plan 1 or Plan 2.

## Viva Insights licenses

[Assign licenses](assign-licenses.md) to the users whose mailboxes you want to analyze. They include all the employees in your organization or a specific subset. To ensure statistical significance and meaningful comparative analysis, companies get the most benefit when they deploy Viva Insights to the entire company or to a large group of employees.

## Pricing

Contact your Microsoft account team for pricing. If you have questions about licensing, have your admin reach out to your Microsoft account team, or use [this form](https://www.microsoft.com/microsoft-viva/buy-insights) to inquire about Viva Insights.

## Supported browsers

For the best experience, use Microsoft Edge or Google Chrome.

Apple Safari and Mozilla Firefox are not preferred browsers for the advanced insights app available with Viva Insights. Internet Explorer is no longer a supported browser.

## Service availability during an outage

Microsoft provides oversight, framework, and tooling to ensure that products like Viva Insights can maintain functionality and recover from a service outage. All Microsoft 365 applications are required to have a Business Continuity and Disaster Recovery (BCDR) plan. 

If there’s an outage, Viva Insights will use a failover process to switch to a backup location. This ensures customers will continue to have access to existing reports, and all organization insights features (Manager/Leader and Analyst/Advanced Insights experience) will still be available. Users, however, won't be able to create new queries and reports until the primary region is back up and running.

Service availability is consistent across environments where Viva Insights plans are generally available. See details at [Microsoft Viva service description - Service Descriptions.](https://learn.microsoft.com/en-us/office365/servicedescriptions/microsoft-viva-service-description)

## Related topics

* Under [Powerful tools to support your enterprise](https://www.microsoft.com/microsoft-365/business/compare-more-office-365-for-business-plans), see **Looking for more** for more details about the available plans
* To provide feedback, go to [Microsoft Office 365 UserVoice forum](https://feedbackportal.microsoft.com/feedback/)

