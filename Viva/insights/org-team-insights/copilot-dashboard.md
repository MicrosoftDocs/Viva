---
ms.date: 11/14/2023
title: Connect to the Microsoft Copilot Dashboard (Preview)
description: Explains how to set up and use the Microsoft Copilot Dashboard, including the update process and frequently asked questions.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Connect to the Microsoft Copilot Dashboard (Preview)

Copilot in Microsoft 365 works alongside you to unleash your creativity and help you perform tasks faster. It helps summarize key points and action items in Microsoft Teams, draft new documents in Word, jumpstart replies in Outlook, and more.

The Microsoft Copilot Dashboard (Preview) from Viva Insights helps organizational leaders prepare for Copilot rollout, track adoption of key features, and assess its impact.

### Prerequisites 

To install the Microsoft Copilot Dashboard (Preview) in Power BI and connect it to your data, make sure you have the following:

* A Microsoft 365 or Office 365 subscription for enterprise or business 

* A Power BI Pro license. If you don’t have a Power BI Pro license, [get a free trial now](https://powerbi.microsoft.com/power-bi-pro/).

* One of the following Microsoft 365 admin roles:
    * Global Administrator
    * Exchange Administrator
    * SharePoint Administrator
    * Teams Communications Administrator
    * Teams Administrator
    * Office Apps Administrator
    * Global Reader
    * Report Reader

You're *not* required to have a Viva Insights subscription to use the report. The report is made available to you as part of your Microsoft 365 or Office 365 subscription.

>[!Note]
>The Microsoft Copilot Dashboard (Preview) is currently not available for national/regional cloud deployments including but not limited to Microsoft’s U.S. Government clouds and Office 365 operated by 21Vianet.

### Install the app

1. Use the following link to get to the app: [Microsoft Copilot Dashboard (Preview)](https://aka.ms/copilot-impact).

1. On the AppSource page for the app, select **Get it now**. You can also search for the app in the Power BI app marketplace.

1. When prompted, select **Install**.

1. When the app finishes installing, it will appear on your Power BI Apps page. Select the app to open it.

1. At the top of the app, select **Connect your data**.

1. In the **Connect to Microsoft Copilot Dashboard** dialog, enter your Microsoft 365 tenant ID. Follow the steps on [this page](/sharepoint/find-your-office-365-tenant-id) to find your tenant ID. When you're done, select **Next**.

   :::image type="complex" source="images/copilot-impact-dashboard-01.png" alt-text="Screenshot that shows the step to enter the tenant Id." lightbox="images/copilot-impact-dashboard-01.png":::
   Screenshot that shows the step to enter the tenant Id.
   :::image-end:::

1. Connect your account:
    * For "Authentication method," select **OAuth2**.
    * For "Privacy level setting for this data source," select **Organizational**.
    * When you're done, select **Sign in and connect**.

1. Select the user account. Make sure to sign in with the credentials that you use for admin access to your Microsoft 365 tenant (see list of approved roles above).

1. Wait for the report to build with your organization’s data. This should occur within several minutes.

### Update the app

Periodically you may receive update notifications from AppSource/Power BI about a new version of the app. When you install the new version, the following options are available:

:::image type="complex" source="images/copilot-impact-dashboard-02.png" alt-text="Screenshot that shows different options for updating the app." lightbox="images/copilot-impact-dashboard-02.png":::
   Screenshot that shows different options for updating the app.
:::image-end:::

Select **Update the workspace and the app**, then select **Install**. This will install the update, overwriting the existing/installed workspace and app.

#### Issues

If you have any issues with the dataset refresh/app update during the update process, use these steps to refresh the dataset and make sure your dataset configurations are set correctly:

1. Go to the workspace panel and open the app workspace.

1. In the dataset settings, select **Scheduled Refresh**.

1. Open the **Parameters** section and configure the data source once again in the **Data Source** section with the credentials with which you have access to the **Tenant ID** with valid permissions, mentioned in the prerequisites section above.

1. Once you complete the above steps, go back to the app workspace and select **Refresh**.

1. Once the dataset has refreshed successfully, select **Update App** at the top-right of the app workspace.

### Interpreting the data
#### Readiness

The information in this table helps you assess your organization’s overall readiness for Copilot rollout based on technical eligibility requirements and overall Microsoft 365 app usage. Note that this tab does not provide a comprehensive summary of all readiness and eligibility requirements. For a full set of requirements see this page: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements).

Unless otherwise mentioned, all metrics on this page represent aggregations over the prior 28 day period. Data points are refreshed daily.

| Metric | Definition | More information |
|---|---|---|
| Total prerequisite licenses |  Count of licenses qualified for Copilot in Microsoft 365.  | In order to be assigned a Copilot license, users must already be assigned a license for Microsoft 365 E3 or E5. Learn more here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#license-requirements)  | 
| Users on eligible app update channels  | Count of users who connected to Microsoft 365 Apps over the past 28 days with a device enrolled in the Current Channel or Monthly Enterprise Channel. **Note:** This information is based on usage signals for Microsoft 365 Apps and may not reflect the most recent status of users’ devices.   | User devices must be on either Current Channel or Monthly Enterprise Channel to access Microsoft 365 Copilot features. In November, Copilot will initially be available on Current Channel, and Monthly Enterprise Channel a month later. Learn more here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#update-channels) | 
| Microsoft 365 app usage  | Count of unique active users per Microsoft 365 app feature, limited to those with Copilot capabilities. **Note:** The list displayed on this page does not include all Microsoft 365 apps with Copilot capabilities. More will be added over time.  | Users must be actively using Microsoft 365 apps in order to benefit from Copilot. Learn more about specific application requirements here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#prerequisites) |

#### Adoption

After you've deployed Copilot in your organization, this page allows you to track user adoption trends per Microsoft 365 app and Copilot feature. Information is consistent with data points displayed in the Microsoft 365 Admin Center including the [Copilot Usage report](/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage) and [Microsoft Adoption Score](/microsoft-365/admin/adoption/adoption-score).

All metrics on this page represent aggregations over the past 28 days. Data points are refreshed daily.

| Metric | Definition |
|---|---|
| User count per application   | Count of unique active users per Microsoft 365 application over the past 28 days. An active user is someone who completed any intentional action in Copilot (e.g., sending a prompt or generating a Word document) at least once during that timeframe. The applications included here are currently limited to Teams, Outlook, Word, Excel, PowerPoint, and OneNote. Microsoft 365 Chat is not yet included in the report. | 
| User count per feature   | Count of unique active users per distinct Copilot feature area. These counts are currently limited to activities in Teams, Word, PowerPoint, and Outlook. More features will be added over time. **Feature definitions:** *Summarize a Teams meeting*: user used Copilot in a Microsoft Teams meeting to summarize the meeting. *Summarize a Teams conversation*: user used Copilot to summarize a Microsoft Teams chat or channel conversation. *Summarize an Outlook email thread*: user used Copilot to summarize an Outlook email thread. *Summarize a Word document*: user used Copilot to summarize a Word document. *Summarize a PowerPoint presentation*: user used Copilot to summarize a PowerPoint presentation. *Draft a Word document*: user used Copilot to create a new Word document. *Create a PowerPoint presentation*: user used Copilot to create a new PowerPoint presentation. *Generate an Outlook email draft*: user used Copilot to generate an email draft in Outlook. *Rewrite a Word document*: user used Copilot to rewrite a Word document.  |
| Actions per user per feature | Average number of actions completed per active user over the past 28 days for each of the features above. This metric only counts the initial step of prompting Copilot to complete some action; it does not include any post-prompt actions such as copying a meeting summary or inserting drafted email text into an email body.  |

#### Impact

This page helps you assess the Copilot impact based on your organization's usage patterns and results from Microsoft's quantitative and qualitative research.

The metrics on this page represent aggregations over the prior 28 days. Data points are refreshed daily.

| Metric | Definition |
|---|---|
| Hours saved across Copilot users  | This is a general estimate of the amount of time Copilot users in your organization are saving each week through use of Copilot features. The figure is calculated by multiplying your count of active Copilot users across apps over the past month (consistent with the definition used in the Adoption tab) by a time savings multiplier derived from [Microsoft’s research on Copilot users](https://aka.ms/m365-ai-impact-research). This multiplier may be updated over time as Microsoft’s research progresses and Copilot features evolve.  | 
| Potential impact for your org: Teams meeting users   | Count of Teams meetings users across your organization over the past 28 days, including both 1:1 and group calls. This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have if extended to all Teams meeting users in your organization.  |
| Potential impact for your org: Chats sent | Average volume of Teams chats sent per week (including group and 1:1 chats). This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have if extended to all Teams chat users in your organization.  |
| Potential impact for your org: Emails sent  | Average volume of emails sent via Exchange per week (note: these emails may not necessarily be delivered through Outlook). This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have if extended to all Outlook email users in your organization. |
| Potential impact for your org: Active cloud files  | Total count of active files in SharePoint and OneDrive over the prior month (learn more about how the SharePoint information is calculated [here](/microsoft-365/admin/activity-reports/sharepoint-site-usage-ww) and OneDrive [here](/microsoft-365/admin/activity-reports/onedrive-for-business-usage-ww)). “Active” means that a file was viewed, modified, downloaded, or shared. This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have if extended to all Office document users in your organization. |

#### News & research

Research around the impacts of AI on workplace productivity is evolving quickly. Use this page to stay up to speed on the latest findings from Microsoft’s own AI research teams.

### FAQs

**Do I need a Viva Insights subscription in order to access the report?**

No, a Viva Insights subscription is not required. The report is available to any customer with a Microsoft 365 or Office 365 subscription for business or enterprise.

**Does the report use Viva Insights data to create any of the metrics?**

No, the report does not use any Viva Insights data in the process of computing the metrics shown. The report is based on your Microsoft 365 tenant’s usage and licensing data. 

**I’m receiving an error at the time of connecting my data with the dashboard. What should I do?**

First, check in the Microsoft 365 Admin Center that you have one of the roles listed in the Prerequisites section above. If you don’t, request this access from your administrator. Then, ensure you’re using the correct Microsoft 365 tenant ID. 

**How do I know that I have the latest version of the template app installed?**

Microsoft may periodically release a new version of the Microsoft Copilot Dashboard in order to deliver new features or update text and visuals in the report. Microsoft will notify your organization of new version releases via the [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?#/MessageCenter). Microsoft 365 Message center. In addition, the user in your organization who installed the application will receive a notification in Power BI requesting that they update to the latest version of the report. That user should follow the steps above to update to the latest version of the app.