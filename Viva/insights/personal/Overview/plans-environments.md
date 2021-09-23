---

title: Plans and environments for personal insights
description: Supported plans and environment requirements for personal insights in Microsoft Viva Insights (formerly MyAnalytics)
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: Mya
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Personal insights plans and environments

Microsoft Viva Insights provides personal insights in [Viva Insights in Teams](../teams/viva-teams-app.md), the [Dashboard](../use/dashboard-2.md), [Briefing emails](../Briefing/be-overview.md), [Digests](../use/email-digest-2.md), [Viva Insights Outlook add-in](../use/add-in.md), and [Inline suggestions](../use/mya-notifications.md).

Users can use the following Viva Insights (MyAnalytics) features whose organization uses the following Microsoft 365 or Office 365 plans:

* **Viva Insights (Full) and Viva Insights Outlook add-in** - Microsoft 365 E5, Microsoft 365 E5 without Audio Conferencing, Office 365 Enterprise E5, Office 365 Nonprofit E5, and Office 365 G5, Workplace Analytics
* **Viva Insights (Full)** - Microsoft 365 A5 for faculty and students and Office 365 A5 for faculty and students
* **Viva Insights Outlook add-in** - Microsoft 365 E3, Microsoft 365 Business, Microsoft 365 A3 for faculty and students, Office 365 E3, Office 365 E1, Office 365 A3 for faculty and students, Office 365 E3 Developer, Office 365 G3, Business Premium, and Business Essentials

>[!Note]
>
>* To find out how to determine your own plan and service plan, see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is).
>* For more information about the plans that offer these user experiences, see [Microsoft 365 business plans](https://products.office.com/business/compare-more-office-365-for-business-plans).

### Features in the Viva Insights (Full) service plan

The following features are available only in the Viva Insights (MyAnalytics, Full) service plan.

* Read-status features: [Email read rates and document open rates](../use/use-the-insights.md#track-email-and-document-open-rates), [Track email](../use/mya-notifications.md#track-email), [Track email open rate](../use/mya-notifications.md#track-email-open-rate)
* [Shorten a meeting](../use/mya-notifications.md#shorten-a-meeting)
* [Delay delivery plan](../use/delay-delivery.md)

## Access to Viva Insights elements

After users get assigned licenses with a Viva Insights (MyAnalytics) service plan, they get access to the following Viva Insights elements based on their service plan.

| Element | Approximate time frame |
| ------- | ------------------|
| [Welcome email](../use/mya-welcome-email.md) | Sent to existing Microsoft 365 users a few days (up to four weeks) after license assignment; sent to new users approximately four weeks after license assignment|
| [Dashboard](../use/dashboard-2.md)  | Available a few days after license assignment |
| [Digests](../use/email-digest-2.md)  | Sent the Monday of the first week after the welcome email |
| [Inline suggestions](../use/mya-notifications.md)  | Available about one day after license assignment |
| [Viva Insights Outlook add-in](../use/add-in.md)  | Available about one day after license assignment |

>[!Note]  
>
>* _Licensed users_ have Viva Insights automatically enabled after license assignment.
>* _All users_ in your organization are opted-in, whether or not they have licenses with a Viva Insights service plan. If you want one or more licensed users to be opted _out_ by default, see [Set access for one user](../setup/configure.md#set-access-for-one-user) and [Set access for multiple users](../setup/configure.md#set-access-for-multiple-users).

## Environment support

### Microsoft 365 environments that are supported

* Worldwide Multi-tenant
* Dedicated Multi-tenant
* Government Community Cloud (GCC)

### Microsoft 365 environments that are not supported

* GCC-High
* DoD
* Microsoft 365 Germany
* Microsoft 365 Operated by 21Vianet

<!-- *NOT* REMOVED 21 APRIL 2021! but there are changes to the Germany situation: * Microsoft 365 Germany  -->

## Browser support

You can use the following web browsers to view your Viva Insights dashboard.

* Microsoft Edge or Edge Chromium (coming soon)
* Microsoft Internet Explorer version 10 or 11
* Google Chrome (latest version)
* Apple Safari (latest version)
* Mozilla Firefox (latest version)

As an Outlook add-in, the Viva Insights Outlook add-in requires a browser compatible with your system's platform and operating system. For details, see [Browsers used by Microsoft 365 add-ins](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins).

## Language support

Viva Insights is available in the same languages as Microsoft 365. See [What languages is Office available in](https://support.office.com/en-ie/article/what-languages-is-office-available-in-26d30382-9fba-45dd-bf55-02ab03e2a7ec).

## Prerequisites and exclusions

* [Microsoft Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-service-description) is required for Viva Insights (Full) and the Viva Insights Outlook add-in.

* **Licensing exclusion** - Shared mailboxes cannot use and are not supported by the Viva Insights service plan.

## Outlook support and prerequisites

* For the Outlook add-in, see [Why don't I see the Viva Insights Outlook add-in](../use/add-in.md#why-dont-i-see-the-outlook-insights-add-in).
* For Inline suggestions, see [Why don't I see any inline suggestions](../use/mya-notifications.md#why-dont-i-see-any-inline-suggestions).
