---
ms.date: 05/22/2023
title: Errors in Viva Insights
description: This article provides a list of errors you could encounter while using Viva Insights, along with solutions 
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

# Errors

If you get one of these errors in the Viva Insights app in Teams and web, or the advanced insights app, read through our solution. If you've tried the solution and you're still getting the same error, [contact our support team](/microsoft-365/admin/get-help-support#online-support) for help.

|App|Action|Error|
|--------|-------|-----|
|**Advanced insights**|Setup/sign-in | [Oops! System is not yet ready to run queries...](#oops-system-is-not-yet-ready-to-run-queries)
|||[Oops! You haven't been assigned a role in Viva Insights yet...](#oops-you-havent-been-assigned-a-role-in-viva-insights-yet)
|||[Oops! Something's wrong and we can't find that page.](#oops-somethings-wrong-and-we-cant-find-that-page) 
||Accessing the **Manager settings** page|[Manager settings can't be edited yet...](#manager-settings-cant-be-edited-yet)
||Viewing the **Organizational data** page|[Oops! Something's wrong and we can't render this page right now. Please try again later.](#oops-somethings-wrong-and-we-cant-render-this-page-right-now)
||Adding organizational data| Validated, processing <br><br>0% of insights using organization data are available due to missing or low-quality data fields<br><br>No data found for selected source<br><br>Another upload or delete action is currently underway. To continue, wait for that action to be completed<br><br>Submission for upload failed. If you already have an upload or delete action in progress, wait for it to finish. Otherwise, please try again.
|**Workplace Analytics**|Any|[It looks like you don’t have access to this space...](#it-looks-like-you-dont-have-access-to-this-space)
|**Viva Insights on Teams and web**|Viewing organization insights|Organization insights aren't showing (no message)
|||[Sorry, something went wrong.](#sorry-something-went-wrong)
|||[This content needs additional organization data](#this-content-needs-additional-organization-data)


## Advanced insights app

### Signing in and setting up the advanced insights app

#### Oops! System is not yet ready to run queries... 

**Please check with Viva Insights Admin if at least 10 licenses have been assigned. If already done, then please wait until we get the system ready for running queries.**

##### Why am I getting this error?

Your setup may not have completed yet or your organization might not have enough licenses assigned.

##### What can I do to resolve it?

It takes a few days for Viva Insights to process Microsoft 365 collaboration data and for assigned users to get the right permissions. Most customers are able to access the app four to five days after the Insights admin assigns licenses.

Contact your Insights Administrator to confirm they've assigned enough licenses. They need to assign at least 10.

##### Where can I go to learn more?

* [Question 4](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) in our FAQ's Setup and configuration section
* [Setup](../setup-maint/setup.md)
* [Assign licenses](../setup-maint/assign-licenses.md)

#### Oops! You haven't been assigned a role in Viva Insights yet...

**Please contact M365 admin for role assignment.**

##### Why am I getting this error?

You might get this error in the advanced insights app, usually on your first sign-in, for one of three reasons:

* Your Microsoft 365 global admin hasn't assigned you a Viva Insights license (that is, the ability to use the advanced insights app).
* Your Insights Administrator hasn't assigned you to a role that can access this page.
* Your organization might use Privileged Identity Management (PIM) as an additional approval process, and you haven't activated your role yet. 

##### What can I do to resolve it?

* Contact your Insights Administrator to confirm they've assigned you the right license and role. 
* Check whether your role has [permissions](../setup-maint/user-roles.md#feature-access) to access this page. 
* If applicable, activate your role in PIM. You can validate and view pending role activations using Azure Active Directory. To find out how to do this, refer to [Activate a role](/azure/active-directory/privileged-identity-management/pim-how-to-activate-role.md#activate-a-role)

##### Where can I go to learn more?

* [Question 4](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) in our FAQ's Setup and configuration section
* [Assign licenses](../setup-maint/assign-licenses.md)
* [Assign roles](../setup-maint/assign-user-roles.md)
* [Feature access](../setup-maint/user-roles.md#feature-access)


#### Oops! Something's wrong and we can't find that page.

Refer to the information in [Oops! You haven't been assigned a role in Viva Insights yet...](#oops-you-havent-been-assigned-a-role-in-viva-insights-yet).

#### It looks like you don’t have access to this space... 

**Go to the new and enhanced Viva Insights platform for the most up-to-date experience.**


##### Why am I getting this error?

You'll get this error on the legacy Workplace Analytics app if you no longer have access to it.

##### What can I do to resolve it?

All customers are given a 90-day period to transition from the legacy Workplace Analytics app to the new advanced insights app. After this period, you'll see this error.

If you want to temporarily access the legacy Workplace Analytics app to retrieve data, contact our support team for help. If you’re only assigned [roles for our new platform](../setup-maint/user-roles.md), you’re not able to access the legacy app.

##### Where can I go to learn more?

* [Introduction to advanced insights](../introduction-to-advanced-insights.md)
* [User roles](../setup-maint/user-roles.md)

### Manager settings page

#### Manager settings can't be edited yet... 

**Please try again in a few days.**

[Pending]

##### Why am I getting this error?

You might get this error on the Manager settings page for two reasons:

* Data processing hasn't completed.
* You might not have the right prerequisites to access the **Manager settings** page.
* Fewer than 10 people in your organization have licenses.

##### What can I do to resolve it?

It takes a few days for Viva Insights to process Microsoft 365 collaboration data and for assigned users to get the right permissions. Most customers are able to access the app four to five days after the Insights admin assigns licenses.

If it's been four to five days:

* Review our documentation to make sure you have the right prerequisites to access **Manager settings**.
* Make sure at least 10 people in your organization have Viva Insights licenses assigned to them.

##### Where can I go to learn more?

### Data upload

#### Oops! Something's wrong and we can't render this page right now...

**Please try again later.**

## Viva Insights app in Teams and web

### Viewing organization insights

#### Sorry, something went wrong

##### Why am I getting this error?

You might not have the right license or roles to access organization insights. Or, your team might not meet the minimum team size. 

##### What can I do to resolve it?

Contact your Insights Administrator to make sure you have the right license and role assigned. 

To view organization insights, you need to have at least the minimum team size, which your admin sets in **Manager settings**. Your team can be made up of direct or indirect reports, but they need to be correctly mapped to you in the organizational your admin uploads to Viva Insights. 

##### Where can I go to learn more?

* [Question 4](faq.md#q4-our-admin-assigned-the-required-licenses-why-cant-insights-analysts-access-the-advanced-insights-app) in our FAQ's **Setup and configuration** section.
* [Assign licenses](../setup-maint/assign-licenses.md)
* [Assign roles](../setup-maint/assign-user-roles.md)
* [Role access](../setup-maint/user-roles.md)
* [Manager settings](../setup-maint/manager-settings.md) (to check your minimum team size)
* [Organization insights](../../org-team-insights/org-insights.md)

#### This content needs additional organization data

Refer to the information in [Sorry, something went wrong](#sorry-something-went-wrong).