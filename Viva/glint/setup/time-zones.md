---
title: Communicate with Viva Glint users based on time zone
description: Microsoft Viva Glint offers the ability to send survey invites, reminders, and other notifications in users’ preferred time zones. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: standard attributes, custom attributes, functional attributes, time zones, languages
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 12/07/2023
---

# Communicate with Viva Glint users based on time zone

Microsoft Viva Glint offers the ability to send survey invites, reminders, and other notifications in users’ preferred time zones. 

> [!NOTE]
> This feature sends emails on a time zone-based schedule but doesn’t include activation/deactivation of each user’s survey by time zone.

## Set up a time zone attribute

In order to ensure employees receive survey communications in their unique time zones, your time zone attribute must be appropriately configured as an optional system attribute. [Learn more](https://go.microsoft.com/fwlink/?linkid=2247991). Once configured, you'll be able to include this time zone attribute in your employee data to trigger survey emails in employees' time zones.
 
Use the Time Zone tab of the [**Employee Attribute Template**](https://www.microsoft.com/download/details.aspx?id=105533) to find valid time zone values. Before a survey launches, ensure that all employees have a valid value attached to their records.

> [!NOTE]
> When a user has a blank or invalid time zone value in employee data, notifications send in the default time zone selected in General Settings.

## Manage time zone options in General Settings

As a Viva Glint admin, select a default time zone and enable sending in users’ time zones in General Settings.

### Set a default time zone

Set the default time zone in the **Company Information** section of **General Settings**, found on the admin dashboard from the configuration page, in the **Service Configuration** section. Use the dropdown menu to find your organization’s default time zone and then select **Save Changes**.

> [!NOTE]
> Employee Lifecycle survey invitations are triggered by events. These events send platform notifications at your Viva Glint default time zone.

## Enable notification in user time zone

Set notifications to **send in users’ time zones** in the **Communication section** of **General Settings**, found on the admin dashboard from the configuration page, in the **Service Configuration** section. Toggle to **YES** to activate and then select **Save Changes**.

This setting applies to all survey and results notification emails and can’t be disabled or enabled at the survey program level. When enabled, a 24-hour buffer is added to survey start and end times to allow for users to access and submit surveys across the globe.

> For example:
> Contoso, with a default time zone/headquarters in New York, wants to ensure that their Sydney, Australia employees receive and access their surveys at the same time in their day as the rest of their employee population. For survey invites to send to Sydney employees at 9:00 AM on March 28 in Australia/Sydney time, the survey will need to be active no later than 12:00 AM, March 27, New York time because New York is 14 hours behind Sydney.

> Enabling sending in user time zone allows for invites to send to users at the appropriate time and to submit their surveys until midnight on April 12 by adding a 24-hour cushion before launch and after survey close.

> | Event: |Survey activation|Survey launch|Survey close|Survey deactivation|
> |:----------------  |:----------------|:------------|:-----------|-------------------|
> | **Activity:** |Surveys generate/activate|Invites send|Survey ends |Surveys inactivated|
> | **Time:** |March 27, 12:00 AM|March 28, 9:00 AM|April 11, 12:00 AM|April 12, 12:00 AM|

> [!NOTE]
> Users in any time zone can access a survey before receiving an email invite after the Survey Activation time if they have access to My Surveys in Viva Glint or with attribute-based survey access. Any results submitted appear in the dashboard at 12:00 AM on the survey launch day.

>[!IMPORTANT]
> If this feature is activated or deactivated during a live survey, the update won't apply to emails and reminders that are already scheduled, and it won't affect the activation date/deactivation dates on existing surveys.

