---
title: JIRA On-Premise Integration for Viva Goals
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
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
description: "Learn how to integrate your Viva Goals OKRs with the JIRA on-premise application."
---

# JIRA On-Premise Integration for Viva Goals

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Who can use this feature? 

All users and administrators (Admins also have permissions to manage the integration from the admin dashboard).

## About the Jira On-Premise Integration

Integrating Jira with Viva Goals enables you to link Jira user stories, epics, and projects with Viva Goals OKRs. Any updates on the linked Jira user stories, epics, or projects will automatically update the progress of linked Viva Goals OKRs. This makes for a powerful setup because it ensures your OKR process is not waiting on manual check-ins and any progress is updated real-time on Viva Goals.

## Connect the JIRA On-Premise App to your Viva Goals account

1. The first step in setting up the integration is to connect your Jira On-premise account to Ally.io. Navigate to your sidebar and click Admin and then click Integrations.
1. In the integrations section, go to Jira and then click on **Enable**. If you’re already created a connection, you’ll see a **Manage** button. Click on **Manage**. 
1. Click **New Connection** and in the pop-up dialog box, add the following details: 
    - **Connection name**: Give your connection name. 
    - **Server**: Add your Jira Server URL. 
    - **How is this Jira instance hosted?**: For this question, select the **Jira-Server** option.  
    - **Account UUID**: The Account UUID will be used in the Jira configuration after you install the **Ally OKRs for JIRA** app from the Atlassian Marketplace.
    - **Access Token**: The Access Token will be used in the Jira configuration after you install the **Ally OKRs for JIRA** app from the Atlassian Marketplace.
    
    :::image type="content" source="../media/goals/jira-create-conn.png" alt-text="Jira create connection":::

## How to install and setup the Viva Goals OKRs for JIRA app from the Atlassian Marketplace

1. As a Jira administrator, search for "Viva Goals OKRs for JIRA" app from the "Manage Apps" page in JIRA.

   :::image type="content" source="../media/goals/manage-apps.png" alt-text="Manage apps":::

2. Click on the install button against the app and follow the steps in the confirm app installation popup.

   :::image type="content" source="../media/goals/app-installation.png" alt-text="App installation":::

3. After the installation is completed, click on **Get Started**.
4. Inside the **Viva Goals OKRs admin** configuration screen, enter the **Account UUID & Access Token**. (Refer Step 3(d)and 3(e) under [Connect Jira On-Premise to your Viva Goals account](https://help.ally.io/en/articles/4258025-jira-on-premise-integration-for-ally-io#h_5e53ba8949) section).

   :::image type="content" source="../media/goals/vivagoals-okrs-admin-conf.png" alt-text="Admin configuration screen":::
   
5. Enter the Account UUID and Access Token and click on **Connect** to validate the credentials. On successful verification, you will see a success banner to return to the connection screen in Viva Goals to complete the setup.

   :::image type="content" source="../media/goals/credentials-verification.png" alt-text="Verification of credentials":::

6. From the connection screen in Viva Goals, Click on **Validate JIRA Connection** to check if Viva Goals has access to JIRA and if everything is set up correctly.

   :::image type="content" source="../media/goals/validate-jira-conn.png" alt-text="Validate JIRA connection":::

7. Click **Next** to finish the connection setup.
8. Once set up, Viva Goals will create a user called **allyokrsforjira** in Jira to track and update progress for connected OKRs and Projects. This user will be able to access the connected Jira projects on behalf of Viva Goals.

> [!NOTE]
> 1. If the user creation in Jira fails during the installation phase, the Jira admin needs to enter the service account details so that the JIRA app can access project details on behalf of Viva Goals. Here are the following details to be added:
> Username = Add an existing Jira username. 
> Password =  Give the respective password for the account.  
> 
> :::image type="content" source="../media/goals/service-account-details.png" alt-text="Service account details":::
> 
> 2. The service account user entered above or the **allyokrsforjira** user created by Viva Goals during the JIRA app installation, should have access to the Jira projects which you intend to connect with Viva Goals. This access is to ensure that the Viva Goals OKRs for JIRA app has access to the Jira project details.

## Using the JIRA Integration

Once the setup is complete, members can link their OKRs directly to stories or Epics in Jira.

1. While creating an Objective or Key Result, click on **Automatically connect from a data source**. 
  
   :::image type="content" source="../media/goals/new-objective.png" alt-text="New objective":::

2. From the list of integrations, pick JIRA.

   :::image type="content" source="../media/goals/choosing-jira.png" alt-text="Choosing JIRA":::

3. Next, select the connection, if multiple exist.
4. Add a JQL query to match any issues that would relate to the Objective, Key Result or Project. This also means that as more issues in Jira match the query, they keep getting linked to the success of the Objective or Key Result.

   :::image type="content" source="../media/goals/jql-query.png" alt-text="JQL query":::

A JQL query can be copied from Jira. Search for issues you want to link to your Objective using available filters on Jira. Next, click on the ‘Advanced’ option and Jira automatically converts your search to a JQL query. You can copy and paste the query string into your integration with Viva Goals.

:::image type="content" source="../media/goals/query-string.png" alt-text="Query string":::

The JQL query linked to the Objective or Key Result can be edited at any time. This leads to a recalculation of current progress.

> [!NOTE]
> If you are using JIRA next-gen projects, the support for JQL can behave slightly differently compared to classic JIRA projects. For example, JIRA next-gen projects do not support queries based on the epic link. Here is an official JIRA quote summarising this scenario, "Users should query on next-gen epics using the parent =. If you want to combine Epics from both project types, an example of such a query would be: "Epic Link" = NPC-6 OR parent = NJDP-5. The Parent field can now be selected as a column in the Global Issue Navigator and exported from Jira."

5. Select the metric you want to use to track progress. If you are tracking by KPI, you will also have the option to track done tickets only or all tickets by toggling the checkbox.

> [!NOTE]
> **Done** tickets include tickets with all statuses that are associated with the JIRA's "Done" workflow status category irrespective of the resolution status of the tickets. [Reference to JIRA article](https://support.atlassian.com/jira-work-management/docs/how-to-create-workflows/).

## Syncing data from JIRA to Viva Goals

Viva Goals pulls in new updates from Jira every 60 minutes. In case you want to track progress immediately, click on Manual sync to sync immediately.

### Current limitation

The automatic sync for the first time will happen within 10 minutes of connecting Jira with an OKR. Please note that OKR progress won’t be synced in the first time sync immediately. However, you can also manually refresh to pull in all the updates by clicking on the **Manual sync** option in the integration pop-up.

Learn more about Ally.io’s other integrations [here](https://help.gotoally.com/integrations).

### FAQs

**Q: How to connect an epic in JIRA so that it does not show 0% progress?**
  
  A: The JIRA integration can show 0% progress even if some tickets that the JQL returns are marked as complete if it is an epic and the JQL entered in Viva Goals is of the form:
   - issue = AI-20
   - "Epic Link" = AI-20
   - cf[10008] = AI-20
   
     In order to resolve this, enter the JQL as "Parent Link" = AI-20 in the JQL field of the JIRA Integration setup in Viva Goals.
