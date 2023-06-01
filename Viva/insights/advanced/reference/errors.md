---
ms.date: 06/01/2023
title: Error messages in Viva Insights
description: Learn how to resolve errors you might encounter in Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Error messages: Viva Insights

This article lists error messages for Viva Insights. We've broken these errors out by app and task:

* [Advanced insights](#advanced-insights)
    * [Sign-in and page access](#sign-in-and-page-access)
    * [Data upload](#data-upload)
* [Workplace Analytics (legacy app)](#workplace-analytics)
* [Viva Insights app in Teams and on the web](#viva-insights-app-in-teams-and-on-the-web)


## Advanced insights

### Sign-in and page access

| Error message | Details |Solution| Resources
|--- | --- |---|---|
| Oops! System is not yet ready to run queries. Please check with Viva Insights Admin if at least 10 licenses have been assigned. If already done, then please wait until we get the system ready for running queries.| Your setup may not have completed yet or your organization might not have enough licenses assigned. | It takes a few days for Viva Insights to process Microsoft 365 collaboration data and for assigned users to get the right permissions. Most customers are able to access the app four to five days after the Insights admin assigns licenses. <br><br> Contact your Insights Administrator to make sure your organization has enough assigned licenses. At least 10 people need to have licenses.  |[Question 4, FAQ](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app)  <br><br>[Setup](../setup-maint/setup.md)<br><br>[Assign licenses](../setup-maint/assign-licenses.md)|
| Oops! You haven't been assigned a role in Viva Insights yet. Please contact M365 admin for role assignment. | You might get this error in the advanced insights app for one of three reasons:<ul><li>Your Microsoft 365 global admin hasn't assigned you a Viva Insights license. <li>Your Insights Administrator hasn't assigned you to a role that can access this page.<li>Your organization might use Privileged Identity Management (PIM) as an additional approval process, and you haven't activated your role yet.  |Contact your Insights Administrator to confirm they've assigned you the right license and role. <br><br>Check whether your role has [permissions](../setup-maint/user-roles.md#feature-access) to access this page. <br><br>If applicable, activate your role in PIM. You can validate and view pending role activations using Azure Active Directory. To find out how to do this, refer to [Activate a role](/azure/active-directory/privileged-identity-management/pim-how-to-activate-role.md#activate-a-role).| [Question 4, FAQ](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) <br><br>[Assign licenses](../setup-maint/assign-licenses.md)<br><br>[Assign roles](../setup-maint/assign-user-roles.md)<br><br>[Feature access](../setup-maint/user-roles.md#feature-access)
|Oops! Something's wrong and we can't render this page right now. Please try again later.| You might not have a license or the right role assigned to access this page.|Contact your Microsoft 365 admin to make sure you have the right license and role assigned.|[Question 4, FAQ](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) <br><br>[Assign licenses](../setup-maint/assign-licenses.md)<br><br>[Assign roles](../setup-maint/assign-user-roles.md)<br><br>[Feature access](../setup-maint/user-roles.md#feature-access)
|Oops! Something's wrong and we can't find that page. | Refer to the information above, in "Oops! Something's wrong and we can't render this page right now..." | |
|Manager settings can't be edited yet. Please try again in a few days.|You might get this error on the **Manager settings** page for three reasons:<ul><li>Data processing hasn't completed. <li>You might not have the right prerequisites to access the **Manager settings** page. <li>Fewer than 10 people in your organization have licenses.|It takes a few days for Viva Insights to process Microsoft 365 collaboration data and for assigned users to get the right permissions. Most customers are able to access the app four to five days after the Insights admin assigns licenses. <br><br>If it's been four to five days: <ul><li>Review our documentation to make sure you have the right prerequisites to access **Manager settings**. <li>Make sure at least 10 people in your organization have Viva Insights licenses assigned to them.| [Assign licenses](../setup-maint/assign-licenses.md)

### Data upload

| Error message | Details |Solution| Resources
|--- | --- |---|---| 
|0% of insights using organizational data are available due to missing or low-quality data fields|You haven't added data to the advanced insights app, and the quality of data from Azure Active Directory is too low. | Add organizational data to the advanced insights app to increase this percentage and unlock different insights.| [Upload organizational data](../admin/upload-org-data-first.md)<br><br>[Data quality](../analyst/data-quality-analyst-experience.md)
|Another upload or delete action is currently underway. To continue, wait for that action to be completed.| You or another admin have added data to the advanced insights app, and it's still processing.|Either wait a few hours for the data to finish processing and refresh the page, or cancel the update and start a new one.| [Upload organizational data](../admin/upload-org-data-first.md)
|Submission for upload failed. If you already have an upload or delete action in progress, wait for it to finish. Otherwise, please try again.|Something caused your upload to fail. |If you don't have another upload in progress, check your file for errors and try uploading it again. If another upload is in progress, wait until it's done processing. Contact our [support team](/microsoft-365/admin/get-help-support#online-support) for help if you keep getting this error.| [Upload organizational data](../admin/upload-org-data-first.md)<br><br> [Support](/microsoft-365/admin/get-help-support#online-support)


## Workplace Analytics

| Error message | Details |Solution| Resources
|--- | --- |---|---|
|It looks like you don’t have access to this space. Go to the new and enhanced Viva Insights platform for the most up-to-date experience.| You'll get this error on the legacy Workplace Analytics app if you no longer have access to it.| All customers are given a 90-day period to transition from the legacy Workplace Analytics app to the new advanced insights app. After this period, you'll see this error.<br><br> If you want to temporarily access the legacy Workplace Analytics app to retrieve data, contact our support team for help. If you’re only assigned [roles for our new platform](../setup-maint/user-roles.md), you’re not able to access the legacy app.| [Introduction to advanced insights](../introduction-to-advanced-insights.md) <br><br> [User roles](../setup-maint/user-roles.md)

## Viva Insights app in Teams and on the web

| Error message | Details |Solution| Resources
|--- | --- |---|---|
|Sorry, something went wrong|You might not have the right license or roles to access organization insights. Or, your team might not meet the minimum team size. |Contact your Insights Administrator to make sure you have the right license and role assigned. <br><br> To view organization insights, you need to have at least the minimum team size, which your admin sets in **Manager settings**. Your team can be made up of direct or indirect reports, but they need to be correctly mapped to you in the organizational your admin uploads to Viva Insights. |[Question 4. FAQ](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) <br><br> [Assign licenses](../setup-maint/assign-licenses.md)<br><br>[Assign roles](../setup-maint/assign-user-roles.md)<br><br>[Role access](../setup-maint/user-roles.md)<br>[Manager settings](../setup-maint/manager-settings.md) (to check your minimum team size) <br><br>[Organization insights](../../org-team-insights/org-insights.md)|
|This content needs additional organization data|Refer to the information above, in "Sorry, something went wrong."

### Missing organization insights

If you can't see organization insights in the Viva Insights app in Teams or on the web, your organization might not have the minimum number of licenses assigned, or you don't meet the minimum team size.

Contact your Insights Administrator to make sure that:

* At least 10 people in your organization have licenses. 
* You have the right license and role assigned to access organization insights.
* Your team members all have licenses, your team meets the minimum team size, and your team members are correctly mapped to you in the organizational data uploaded to Viva Insights.


## Next steps

If you've tried the provided solution to your error and you're still getting the same message, [contact our support team](/microsoft-365/admin/get-help-support#online-support) for help.

