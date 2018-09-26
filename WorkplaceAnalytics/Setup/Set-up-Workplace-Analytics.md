---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup Checklist
description: Complete the steps in this checklist to implement Workplace Analytics in your organization
author: madehmer
ms.author: paul9955
ms.date: 08/08/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Workplace Analytics Setup Checklist

To successfully set up and implement Workplace Analytics, you need to coordinate and get information and buy-in from a variety of stakeholders.

Use the following checklist to help assemble the people and get the data and configuration information that you need to set up and use Workplace Analytics.

> [!TIP]
> This checklist outlines recommended steps and a high-level list of items to consider. It is not intended to be exhaustive. You might want to copy this checklist into a spreadsheet and then customize it for your organization.

### Video: Overview for admins

<!-- OLD INTRO TEXT: To quickly obtain an understanding of how Workplace Analytics works and learn about the initial steps for getting Workplace Analytics up and running, watch the following video: -->

<!-- previous attempts:
1. didn't work:
[Admin overview video](https://aka.ms/WpAAdminOverview_Video)
2. didn't work: 
[<img src="../Images/WpA/setup/Admin-overview-sm.png" alt="Admin overview video">](https://aka.ms/WpAAdminOverview_Video)
3. didn't work: 
<iframe width="640" height="564" src="https://aka.ms/WpAAdminOverview_Video" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>
4. Didn't show the thumbnail specified under id=""
<iframe width="640" height="564" id="../Images/WpA/setup/Admin-overview-sm.png" src="https://player.vimeo.com/video/282383279" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>
5. This works: 
-->

<iframe width="640" height="564" src="https://player.vimeo.com/video/282873274" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## Preliminary review task

To prepare for setting up Workplace Analytics, review the following article:  

| Review this article | Owner | Outcome |
|------|-------|---------|
| [Environment and support aspects of Workplace Analytics](#environment-and-support) | Workplace Analytics administrator |  <!-- VERIFY THIS WORDING --> Confirm that all requirements are in place for setting up Workplace Analytics. Learn about Workplace Analytics licenses, trials, and FastTrack options.  |

## Setup task checklist

To set up Workplace Analytics, complete the following tasks:

| | Task | Owners | Outcome |
|---|------|-------|---------|
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 1 - Determine key personas and assign roles for implementation](#step-1-determine-key-personas-and-roles-for-implementation) |Workplace Analytics sponsor (the initial point-person for the engagement)       |   A list of people in your organization with key roles identified     |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 2 - Assign licenses to population in scope for analysis](#step-2-assign-licenses-to-the-population-in-scope-for-analysis)     |   Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator     | Office 365 licenses are assigned for the population that will be analyzed   |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 3 - Assign roles to Workplace Analytics Admins and Analysts](#step-3-assign-roles-to-workplace-analytics-admins-and-analysts) | Office 365 global administrator   |     Workplace Analytics roles are assigned so that administrators can use Workplace Analytics to set system defaults, privacy settings, and upload and verify organizational data. And,  data analysts can log into and use Workplace Analytics once data is provisioned.   |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 4 - Configure Workplace Analytics settings](#step-4-configure-workplace-analytics-settings) |    Workplace Analytics sponsor, Workplace Analytics administrator   |  Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service by using these rules. Default time zone values are defined in Workplace Analytics.  |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 5 - Prepare and upload organizational data](#step-5-prepare-and-upload-organizational-data)    |   Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst     |    Workplace Analytics administrators have determined what kind of organizational data to provide and how to upload the data. See [Prepare organizational data](../Setup/Prepare-organizational-data.md) and then [Upload organizational data](../Setup/Upload-organizational-data.md).    |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 6 - Validate and verify data](#step-6-validate-and-verify-data)    |  Workplace Analytics administrator, data analysts with full access     |    Workplace Analytics administrators are comfortable that data has been provisioned successfully, data analysts are comfortable with the data and ready to use Workplace Analytics for their analysis.     |
| <img src="../images/wpa/setup/team-adopt-plan-checklist-box.PNG">  | [Step 7 - Set up meeting exclusions](#step-7-set-up-meeting-exclusions)  |   Workplace Analytics administrator, data analysts with full access     |     Workplace Analytics administrators and analysts are satisfied that meeting query results are focused on the data relevant for analysis.

When you have finished all these steps, you are ready to [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md).

## Preliminary review task

### Environment and support

[!INCLUDE [Environment and support](../Setup/Environment-Requirements.md)]

## Setup task details

### Step 1: Determine key personas and roles for implementation

[!INCLUDE [Determine key personas and roles](../Setup/Determine-key-personas.md)]

### Step 2: Assign licenses to the population in scope for analysis

[!INCLUDE [Assign licenses to population](../Setup/Assign-licenses-to-population.md)]

### Step 3: Assign roles to Workplace Analytics admins and analysts

[!INCLUDE [Assign roles to admins and analysts](../Setup/Assign-roles-to-wpa-admins.md)]

### Step 4: Configure Workplace Analytics settings

[!INCLUDE [Configure Workplace Analytics settings](../Setup/Configure-wpa-settings.md)]  

### Step 5: Prepare and upload organizational data

[!INCLUDE [Prepare and upload organizational data](../Setup/Prep-upload-org-data.md)]

### Step 6: Validate and verify data

[!INCLUDE [Validate and verify data](../Setup/Validate-verify-data.md)]

### Step 7: Set up meeting exclusions

[!INCLUDE [Set up meeting exclusions](../Setup/Set-up-mtg-exclusions.md)]
