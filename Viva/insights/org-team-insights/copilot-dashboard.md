---
ms.date: 12/19/2023
title: Connect to the Microsoft Copilot Dashboard (Preview)
description: Explains how to set up and use the Microsoft Copilot Dashboard, including admin controls, the update process, and frequently asked questions.
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

>[!Important]
>This feature is in public preview. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

Copilot for Microsoft 365 works alongside you to unleash your creativity and help you perform tasks faster. It helps summarize key points and action items in Microsoft Teams, draft new documents in Word, jumpstart replies in Outlook, and more.

The Microsoft Copilot Dashboard (Preview) in Viva Insights helps organizations maximize the value of Copilot for Microsoft 365. It provides actionable insights to help your organization get ready to deploy AI, drive adoption based on how AI is transforming workplace behavior, and measure the impact of Copilot.

The dashboard covers the following categories of metrics: Readiness, adoption, impact, and sentiment. Metrics are aggregated at the tenant level.

For customers who are part of the preview, the dashboard is automatically available to select users within the Viva Insights app.

Additionally, the dashboard is broadly available within Power BI, and the dashboard can be installed by admins.

:::image type="complex" source="images/copilot-dashboard-06.png" alt-text="Screenshot that shows the Copilot Dashboard." lightbox="images/copilot-dashboard-06.png":::
Screenshot that shows the Copilot Dashboard.
:::image-end:::

>[!Note]
>The Microsoft Copilot Dashboard (Preview) is currently not available for national/regional cloud deployments including but not limited to Microsoft’s U.S. Government clouds and Office 365 operated by 21Vianet.

## Access the dashboard in Viva Insights

*Applies to: Employee users*

If you have access to the Copilot Dashboard, you can find it in the [Teams or web app](https://insights.cloud.microsoft/#/CopilotDashboard).

1. Open the Teams app on desktop or the web. If you have the Viva Insights app pinned, select it from the left bar.
    * If you don’t have the Viva Insight app pinned, select the ellipses on the left. Then in the search field, enter **Microsoft Viva Insights**, and select it.

2. On the left navigation panel, select **Copilot Dashboard**.

3. To learn more about the data in the dashboard, refer to [Interpreting the dashboard data](#interpreting-the-data).

## Manage user access to the dashboard in Viva Insights

*Applies to: Global admins*

In Viva Insights, the Copilot Dashboard is accessible in the Microsoft Teams and web app. Access controls are managed by Global admins.

For customers who use Microsoft Entra ID (formerly known as Azure Active Directory) to manage user profile data like organization or manager data, the Copilot Dashboard is automatically available to a limited number of users. On average, 3-5 users will be enabled by default.  Access is based on AAD Data, specifically the manager hierarchy attribute. Global admins can disable access at any time.  

**How default-on access is determined**

Users who are senior leaders within large teams as determined by their AAD data manager attribute can automatically view the report. Tenants must meet all of the following criteria to qualify:

* The majority of users in the tenant have the Manager ID attribute assigned
* The majority of users in the tenant are part of a single reporting line
* The tenant has more than 2,500 seats

For those qualifying tenants, only users who meet both of the following criteria are enabled by default:

* The user’s in the top two levels in the organization
* The user has a significant portion of the organization in their reporting line

The criteria above are analyzed on a weekly basis to capture any major org changes. Each week, any new users who meet the above criteria will gain access to the dashboard. The M365 Global Admin can revoke access to those users through the M365 Admin Center (MAC) and they will not be added back unless the admin re-enables them. In addition, admins can disable access to the Copilot Dashboard for their entire organization.

To see how many employees have automatic access to the dashboard and to manage that access, use the process below.

### Manage access for individual users

In the [M365 Admin Center](https://admin.microsoft.com/adminportal/home?#/viva/insights):  

1. Go to the setup tab and select **Microsoft Viva**, then **Viva Insights**. You'll need to enter your credentials if you're not already signed in.  

2. Under **Viva Insights in Microsoft 365**, select **Manage settings for viewing the Copilot dashboard**.  

3. To see how many employees have automatic access, at the top, select **General**.

   :::image type="complex" source="images/copilot-dashboard-02b.png" alt-text="Screenshot that shows how to view the number of employees with access." lightbox="images/copilot-dashboard-02b.png":::
   Screenshot that shows how to view the number of employees with access.
   :::image-end:::

**To enable access for new report users:**

1. Select **Add users**.
1. Search for the people you'd like to add, and select them from the list.
1. At the bottom, select **Add**.

   :::image type="complex" source="images/copilot-dashboard-03.png" alt-text="Screenshot that shows how to add new users." lightbox="images/copilot-dashboard-03.png":::
   Screenshot that shows how to add new users.
   :::image-end:::

**To disable access for existing report users:**

1. At the top, select **Assigned**.
1. Select the users from the list for whom you'd like to remove access.
1. Select **Remove user**.

   :::image type="complex" source="images/copilot-dashboard-04.png" alt-text="Screenshot that shows how to remove users." lightbox="images/copilot-dashboard-04.png":::
   Screenshot that shows how to remove users.
   :::image-end:::

>[!Note]
>Employees can view the dashboard in the Viva Insights Teams or web app. To install the Teams app, please use [these instructions](/Viva/insights/advanced/setup-maint/setup-overview.md) (it is on by default).

### Remove access to the dashboard for the entire tenant with Powershell

You can set a policy to disable the dashboard for the tenant using Powershell cmdlets. Please note that no users will be able to access the dashboard until you remove or update the policy, even if they were added in the M365 Admin Center using the process above. Before you can use the cmdlet, you’ll need to install a module and sign in to be authenticated.

1. [Connect to Exchange Online](/Viva/insights/advanced/setup-maint/configure-personal-insights#connect-to-exchange-online) and, when prompted, sign in with your admin credentials.
1. After you’ve signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet: [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy).

## Install, share, and update the dashboard in Power BI

*Applies to: Admins*

The Copilot Dashboard is also available as an app within Power BI.

To install the dashboard in Power BI and connect it to your data, make sure you have the following:

* A Microsoft 365 or Office 365 subscription for enterprise or business 

* A Power BI Pro license. If you don’t have a Power BI Pro license, [get a free trial now](https://powerbi.microsoft.com/power-bi-pro/).

* One of the following Microsoft 365 admin roles:
    * Global Administrator
    * Exchange Administrator
    * SharePoint Administrator
    * Teams Communications Administrator
    * Teams Administrator
    * Usage Summary Reports Reader
    * Office Apps Administrator
    * Global Reader
    * Report Reader

You're *not* required to have a Viva Insights subscription to use the report, and data stored in Viva Insights is not used to produce the report. The report is made available to you as part of your Microsoft 365 or Office 365 subscription. All data flows for the report are handled in a manner consistent with all applicable Microsoft privacy, security, and compliance commitments and the corresponding data flow requirements.

:::image type="complex" source="images/copilot-impact-dashboard-03.png" alt-text="Screenshot that shows the readiness page in the Copilot Dashboard." lightbox="images/copilot-impact-dashboard-03.png":::
Screenshot that shows the readiness page in the Copilot Dashboard.
:::image-end:::

### Install and share the app

1. Use the following link to get to the app: [Microsoft Copilot Dashboard (Preview)](https://aka.ms/copilot-impact).

1. On the AppSource page for the app, select **Get it now**. You can also search for the app in the Power BI app marketplace.

1. When prompted, select **Install**.

1. When the app finishes installing, it will appear on your Power BI Apps page. Select the app to open it.

1. At the top of the app, select **Connect your data**.

1. In the **Connect to Microsoft Copilot Dashboard** dialog, enter your Microsoft 365 tenant ID. Follow the steps on [this page](/sharepoint/find-your-office-365-tenant-id) to find your tenant ID. When you're done, select **Next**.

1. Connect your account:
    * For "Authentication method," select **OAuth2**.
    * For "Privacy level setting for this data source," select **Organizational**.
    * When you're done, select **Sign in and connect**.

1. Select the user account. Make sure to sign in with the credentials that you use for admin access to your Microsoft 365 tenant (see list of approved roles above).

1. Wait for the report to build with your organization’s data. This should occur within several minutes.

1. Follow the guidelines on [this page](/power-bi/connect-data/service-template-apps-install-distribute#customize-and-share-the-app) to share the app with users in your organization.

>[!Note]
>Please be aware that after you connect your tenant's data to the dashboard, it will be stored outside of the Microsoft 365 service boundary, and might be subject to different security and privacy standards.

### Update the app

Periodically you may receive update notifications from AppSource/Power BI about a new version of the app. After selecting the notification, select **Update the workspace and the app**. Then, select **Install**.

This will install the update, overwriting the existing/installed workspace and app. After completing this step, follow the steps outlined [here](/power-bi/connect-data/service-template-apps-install-distribute#customize-and-share-the-app) to republish the app for users in your organization.

#### Issues

If you have any issues with the dataset refresh/app update during the update process, use these steps to refresh the dataset and make sure your dataset configurations are set correctly:

1. Go to the workspace panel and open the app workspace.

1. In the dataset settings, select **Scheduled Refresh**.

1. Open the **Parameters** section and configure the data source once again in the **Data Source** section with the credentials with which you have access to the **Tenant ID** with valid permissions, mentioned in the prerequisites section above.

1. Once you complete the above steps, go back to the app workspace and select **Refresh**.

1. Once the dataset has refreshed successfully, select **Update App** at the top-right of the app workspace.

## Interpreting the data
### Readiness

The information in this table helps you assess your organization’s overall readiness for Copilot rollout based on technical eligibility requirements and overall Microsoft 365 app usage. Note that this tab does not provide a comprehensive summary of all readiness and eligibility requirements. For a full set of requirements see this page: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements).

Unless otherwise mentioned, all metrics on this page represent aggregations over the prior 28 day period.

| Metric | Definition | More information |
|---|---|---|
| Total prerequisite licenses |  Count of licenses qualified for Copilot in Microsoft 365.  | In order to be assigned a Copilot license, users must already be assigned a license for Microsoft 365 E3 or E5. Learn more here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#license-requirements)  | 
| Users on eligible app update channels  | Count of users who connected to Microsoft 365 Apps over the past 28 days with a device enrolled in the Current Channel or Monthly Enterprise Channel. **Note:** This information is based on usage signals for Microsoft 365 Apps and may not reflect the most recent status of users’ devices.   | User devices must be on either Current Channel or Monthly Enterprise Channel to access Microsoft 365 Copilot features. In November, Copilot will initially be available on Current Channel, and then will be made available on Monthly Enterprise Channel on December 12. Learn more here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#update-channels) | 
| Microsoft 365 app usage  | Count of unique active users per Microsoft 365 app feature, limited to those with Copilot capabilities. **Note:** The list displayed on this page does not include all Microsoft 365 apps with Copilot capabilities. More will be added over time.  | Users must be actively using Microsoft 365 apps in order to benefit from Copilot. Learn more about specific application requirements here: [Microsoft 365 Copilot requirements](/microsoft-365-copilot/microsoft-365-copilot-requirements#prerequisites) |

### Adoption

After you've deployed Copilot in your organization, this page allows you to track user adoption trends per Microsoft 365 app and Copilot feature. Information is consistent with data points displayed in the Microsoft 365 Admin Center including the [Copilot Usage report](/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage) and [Microsoft Adoption Score](/microsoft-365/admin/adoption/adoption-score).

All metrics on this page represent aggregations over the past 28 days with a typical delay of 2-3 days. (For example, if you're viewing the report on a Monday, the data shown would represent the 28-day period ending on the most recent Friday or Saturday).

| Metric | Definition |
|---|---|
| User count per application   | Count of active Copilot users per Microsoft 365 application over the past 28 days. An active user is someone who completed any intentional action in Copilot (e.g., sending a prompt or generating a Word document) at least once during that timeframe. The applications included here are currently limited to Teams, Outlook, Word, Excel, PowerPoint, and OneNote. Microsoft 365 Chat is not yet included in the report. | 
| User count per feature   | Count of unique active users per Copilot feature. These counts are currently limited to activities in Teams, Word, PowerPoint, and Outlook. More features will be added over time. <br /> <br /> **Feature definitions:** <br /> • *Summarize a Teams meeting*: user used Copilot to summarize a Teams meeting. [Learn more about this feature.](https://support.microsoft.com/office/get-started-with-copilot-in-microsoft-teams-meetings-0bf9dd3c-96f7-44e2-8bb8-790bedf066b1) <br> <br />• *Summarize a Teams conversation*: user used Copilot to summarize a Microsoft Teams chat or channel conversation. [Learn more about this feature](https://support.microsoft.com/office/use-copilot-in-microsoft-teams-chat-and-channels-cccccca2-9dc8-49a9-ab76-b1a8ee21486c). <br> <br /> • *Summarize an Outlook email thread*: user used Copilot to summarize an Outlook email thread. [Learn more about this feature](https://support.microsoft.com/office/summarize-an-email-thread-with-copilot-a79873f2-396b-46dc-b852-7fe5947ab640). <br> <br />• *Summarize a Word document*: user used Copilot to summarize a Word document. [Learn more about this feature](https://support.microsoft.com/office/create-a-summary-of-your-document-with-copilot-79bb7a0a-3bf7-41fe-8c09-56f855b669bf). <br> <br />• *Draft a Word document*: user used Copilot to create a new Word document. [Learn more about this feature](https://support.microsoft.com/office/draft-and-add-content-with-copilot-in-word-069c91f0-9e42-4c9a-bbce-fddf5d581541). <br> <br /> • *Create a PowerPoint presentation*: user used Copilot to create a new PowerPoint presentation. [Learn more about this feature](https://support.microsoft.com/office/create-a-new-presentation-3222ee03-f5a4-4d27-8642-9c387ab4854d). <br> <br />• *Generate an Outlook email draft*: user used Copilot to generate an email draft in Outlook. [Learn more about this feature](https://support.microsoft.com/office/draft-an-outlook-email-message-with-copilot-3eb1d053-89b8-491c-8a6e-746015238d9b). <br> <br /> • *Rewrite a Word document*: user used Copilot to rewrite text in a Word document. [Learn more about this feature](https://support.microsoft.com/office/transform-your-content-with-copilot-in-word-923d9763-f896-4da7-8a3f-5b12c3bfc475). |
| Actions per user per feature | Average number of actions completed per active user over the past 28 days for each of the features above. This metric only counts the initial step of prompting Copilot to complete some action; it does not include any post-prompt actions such as copying a meeting summary or inserting drafted email text into an email body. <br /> <br /> This metric helps you assess the intensity of use of each Copilot feature and the degree to which users have come to rely on Copilot for key productivity workflows. For example, if you have 100 users for the “Summarize a Teams meeting” feature and an actions per user value of 10, that means that on average each of those 100 users prompted Copilot in Teams meetings 10 times over the past 28 days (amounting to 1,000 prompts overall).   |

### Impact

This page helps you assess Copilot impact by layering the results of Microsoft's quantitative and qualitative research on top of your organization's Copilot and Microsoft 365 usage patterns.

The metrics on this page represent aggregations over the prior 28 days with a typical delay of 2-3 days. (For example, if you're viewing the report on a Monday, the data shown would represent the 28-day period ending on the most recent Friday or Saturday.)

| Metric | Definition |
|---|---|
| Hours saved across Copilot users over the past 28 days  | This is a general estimate of the amount of time Copilot users in your organization saved over the past 28 days through use of Copilot features. The figure is calculated by multiplying your count of active Copilot users across apps over the past month (consistent with the definition used in the Adoption tab) by a weekly time savings multiplier derived from [Microsoft’s research on Copilot users](https://aka.ms/m365-ai-impact-research), then multiplying that number by four. This multiplier may be updated over time as Microsoft’s research progresses and Copilot features evolve.  | 
| Teams meeting users over past 28 days   | Count of Teams meetings users across your organization over the past 28 days, including both 1:1 and group calls. This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have on users in your organization given their existing usage of Microsoft 365 apps and features. |
| Average Teams chats sent over past 28 days | Average volume of Teams chats sent per week (including group and 1:1 chats). This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have on users in your organization given their existing usage of Microsoft 365 apps and features. |
| Average emails sent over past 28 days | Average volume of emails sent via Exchange per week (note: these emails may not necessarily be delivered through Outlook). This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have on users in your organization given their existing usage of Microsoft 365 apps and features. |
| Active cloud files over past 28 days  | Total count of active files in SharePoint and OneDrive over the prior month (learn more about how the SharePoint information is calculated [here](/microsoft-365/admin/activity-reports/sharepoint-site-usage-ww) and OneDrive [here](/microsoft-365/admin/activity-reports/onedrive-for-business-usage-ww)). “Active” means that a file was viewed, modified, downloaded, or shared. This metric is not based on Copilot usage and is intended to convey the potential impact Copilot could have on users in your organization given their existing usage of Microsoft 365 apps and features. |

### Sentiment

This page provides information that helps you assess Copilot impact from the perspective of users' subjective experiences. In the main table on this page you’ll see a list of Microsoft’s recommended Copilot survey questions along with the results from your own organization’s latest survey (if an admin chooses to upload results for visualization here) and Microsoft’s own benchmark results from [a study of early Copilot users](https://aka.ms/m365-ai-impact-research).

**Suggested Copilot survey questions**

To measure Copilot user sentiment in your organization, we recommend delivering a survey to users in which you ask them to indicate the extent to which they agree with the following four statements:

* *Using Copilot helps improve the quality of my work or output*
* *Using Copilot helps me spend less mental effort on mundane or repetitive tasks*
* *Using Copilot allows me to complete tasks faster*
* *When using Copilot I am more productive*

For each of these, we recommend allowing users to indicate whether or not they Strongly Disagree, Disagree, Neither Agree Nor Disagree, Agree, or Strongly Agree with the statement. You can then combine the “Agree” and “Strongly Agree” responses to compute the % of users who agreed with each statement and compare results with the Microsoft benchmarks shown in this tab.

Your user survey does not need to be limited to these four statements, but we recommend including them at a minimum for easy comparison with Microsoft’s benchmark results.

**Upload survey results through the Microsoft 365 Admin Center**

Microsoft 365 admins can upload survey results through Adoption Score in the Microsoft 365 Admin Center. The results then appear in the Microsoft Copilot Dashboard. [Learn how to upload survey data](/microsoft-365/admin/adoption/ai-assistance?view=o365-worldwide#upload-survey-data&preserve-view=true).

### News & research

Research around the impacts of AI on workplace productivity is evolving quickly. Use this page to stay up to speed on the latest findings from Microsoft’s own AI research teams.

## FAQs

**Do I need a Viva Insights subscription in order to access the report?**

No, a Viva Insights subscription is not required. The report is available to any customer with a Microsoft 365 or Office 365 subscription for business or enterprise.

**Does the report use Viva Insights data to create any of the metrics?**

No, the report does not use any Viva Insights data in the process of computing the metrics shown. The report is based on your Microsoft 365 tenant’s usage and licensing data and is made available to you as part of your Microsoft 365 or Office 365 subscription.

**The values I'm seeing are just "--," with a banner that reads, "Not enough activity data from the past 28 days to show all insights." What's happening?**

To protect individual privacy, you'll only see aggregated insights when there are more than 25 active users.

**I’m receiving an error at the time of connecting my data with the dashboard in Power BI. What should I do?**

First, check in the Microsoft 365 Admin Center that you have one of the roles listed in the Prerequisites section above. If you don’t, request this access from your administrator. Then, ensure you’re using the correct Microsoft 365 tenant ID. 

**How do I know that I have the latest version of the template app installed in Power BI?**

Microsoft may periodically release a new version of the Microsoft Copilot Dashboard in order to deliver new features or update text and visuals in the report. Microsoft will notify your organization of new version releases via the [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?#/MessageCenter). In addition, the user in your organization who installed the application will receive a notification in Power BI requesting that they update to the latest version of the report. That user should follow the steps above to update to the latest version of the app.

**What is the time frame for the data in the Microsoft Copilot Dashboard?**

The dashboard displays data for a rolling 28-day period.