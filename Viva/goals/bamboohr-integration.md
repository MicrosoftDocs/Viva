---
title: "BambooHR Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to automatically provision users & sync employee information to Viva Goals with our seamless BambooHR API Integration."
---

# BambooHR Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

If your organization is using **BambooHR** HRIS for employee management, our API integration enables easy provisioning of new users & updating info of existing users within Viva Goals.

> [!NOTE]
> This Integration feature is accessible for Admins on the Viva Goals app.

To set-up your Viva Goals <> BambooHR integration, perform the following three steps:

1. Enable the Integration on Viva Goals from **Admin -> Integrations -> HRIS Integrations**

    :::image type="content" source="../media/goals/viva-goals-bamboohr-Integration-1.png" alt-text="BambooHR integration 1":::

2. Configure the connection credentials by providing a **Connection Name** (name of your choice to locate the connection in Viva Goals later), **BambooHR API Key**  (instructions below) and **BambooHR sub-domain** (Example: allydemo.bamboohr.com)

    :::image type="content" source="../media/goals/viva-goals-bamboohr-Integration-2.png" alt-text="BambooHR integration 2":::

    To generate an API key, a BambooHR user with adequate permissions should log in and select their name in the upper right-hand corner of any page to get to the user context menu. If they have sufficient permissions, there will be an **API Keys** option in that menu to go to the page and generate the API key as in the following image.

    A non-employee user can be set-up on BambooHR with custom access levels that only includes access to the fields needed for the integration. The API key has the same amount of access as the user who creates it. By setting up the custom access level for this user first, the API key won't have access to more information than necessary.

    :::image type="content" source="../media/goals/viva-goals-bamboohr-Integration-3.png" alt-text="BambooHR integration 3":::

3. Map **Standard Viva Goals fields** with your BambooHR fields

    :::image type="content" source="../media/goals/viva-goals-bamboohr-Integration-4.png" alt-text="BambooHR integration 4":::

Once the three steps are successfully configured and saved, Viva Goals executes an auto-sync of mapped employee information from BambooHR to Viva Goals every day.

## FAQs

### Does Viva Goals sync all Employees from BambooHR?

Currently, Viva Goals pulls all the Employees from your BambooHR instance and sets them up as **Provisioned** users. These users should be explicitly invited from Viva Goals (or) they should log in to Viva Goals themselves for becoming **Active** users who would be billed.

### What fields in Viva Goals can be synced from BambooHR?

All the Viva Goals Standard fields - **User Email**, **First Name**, **Last Name**, **Teams** (comma-separated list of teams that a user is part of), **Manager Email**, **Deactivation Date** (Employee Termination Date) - are available to be synced from BambooHR.

### What is the Matching key field/Unique identifier for a User?

User Email will be the universal match key within Viva Goals. All employee emails from BambooHR, which match Viva Goals User Email will qualify for field updates and new employee emails that don't already exist within Viva Goals will be created as provisioned users.

### Will BambooHR sync over-ride any manual updates within Viva Goals?

Yes! Any sync from BambooHR will over-ride all manual updates to the User profile within Viva Goals.

### How does Deactivation Date work?

The Employee Termination Date recorded within BambooHR should be mapped to Viva Goals' Deactivation Date. Based on the date updated, any user will be deactivated within Viva Goals by the end of that particular date.

### When does the Integration Sync happen?

The Viva Goals <> BambooHR sync is configured to happen daily at 12 AM PST for all organizations.  
  
Reach out to Viva Goals Support to get further details/FAQs answered.
