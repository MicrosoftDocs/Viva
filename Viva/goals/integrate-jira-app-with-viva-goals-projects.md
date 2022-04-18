---
title: Integrate Jira App with Viva goals Projects
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
description: "Connect your Jira epics, tasks, stories, and bugs directly to Viva Goals OKRs, projects and track how execution impacts business outcomes."
---

# Integrate Jira app with Viva Goals projects

> [!IMPORTANT] 
>  Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to Jira app integration

Connecting Jira issues with Viva Goals projects brings updates on connected Jira epics to automatically track OKR progress in Viva Goals. The integration helps in bringing greater context to the engineering team on how their day-to-day work ladders up to the team or company’s goals and the business outcomes. 

Say, for example, a Product Manager links the objective (‘Improve product stability’) with an epic in Jira. As stories within the epic get done, the objective gets closer to its goal. 

The Engineering team resolves to fix 50 UI bugs in a quarter. They create a project for the epic under which all bugs get filed, align the project with an objective, and set the target of their KPI success metric to 50. As the number of bugs filed under the epic is resolved, the progress gets automatically updated in the Viva Goals project and the objective. Every member of the Engineering team can easily get clarity and measure how their work contributed to the objective’s progress. (‘Improve product stability’) 

> [!NOTE]
> The Jira App - Viva Goals integration works only with Viva Goals projects currently. To enable Projects in Viva Goals, click on the 'OKR Model Configuration' section in the Admin Dashboard and select the 'Enable Projects' checkbox and save.

## Pre-requisites to set up the application

1. It's recommended to keep two tabs open since the setup involves going back and forth between the two tabs:

    - Viva Goals Application 
    - Jira Application 

2. The user setting up the app has to be an admin both on the Viva Goals side and on the Jira side, the email ID to be used on both the Jira and the Viva Goals side while setting up has to be the same.

## Setting up the Jira integration 

#### 1. Install the Viva Goals OKRs app from the Jira marketplace

- Go to Apps from the top menu bar, select “Find new apps” from the options and in the next screen search for “Viva Goals OKRs”

- Select the Viva Goals OKRs app and select  **Install App**, in a few minutes the app will get installed with a success message stating that “App added successfully" will be displayed on the screen.

#### 2. Setting up the Jira app on the Viva Goals side

Once the app is installed successfully, select the **Settings** icon and select ‘Apps’ from the dropdown. Select ‘Manage apps’ from the side navigation and select the Viva Goals OKRs for the Jira app to navigate to Viva Goals’ app settings. 

The Viva Goals settings page will contain a set of instructions that will enable the integration, along with a field to enter your Jira API key. To generate your Jira API key, select the **Settings** icon in your Jira instance and select **Atlassian account settings** from the dropdown. On the account settings page, select ‘Security’ from the side nav. Select **Create and manage API tokens** in the API token section to generate a new API token. 

:::image type="content" source="../media/goals/goals-create-jira-api-token.gif" alt-text="Image of create API taken"::: 

- Go to Admin and navigate to the “Integrations” section and search for “Jira App” - there are two versions of Jira in the integration. 

    1. Jira (without an App suffix) 
    1. Jira App - which was is needed to set up this version of Jira

- Against Jira App, select **Manage** to enable the integration. 

    :::image type="content" source="../media/goals/goals-Jira-integration-manage.png" alt-text="Image of Jira integration Manage":::

- Select **New Connection** to add a new connection. 

    :::image type="content" source="../media/goals/goals-create-new-connection.png" alt-text="Image of ceate new connection":::

- Add the connection name, Jira server, Email, Token (paste the API token copied over from Jira) and select **Next** to validate your Jira credentials.

    :::image type="content" source="../media/goals/goals-validate-jira-credentials.png" alt-text="Image of validate your Jira credentials":::

- Once your connection is validated and created, copy the 'Authorization Token' shown in the 'Connect to Jira App' dialog, select the **Apps** section in Jira and select the 'Viva Goals OKRs for Jira' app. Paste the authorization token in the 'Setup Viva GoalsOKRs for Jira' page that follows.  

    :::image type="content" source="../media/goals/goals-authorization-token.png" alt-text="Image of authorize token":::

    :::image type="content" source="../media/goals/goals-paste-ally-auth-token-in-jira.png" alt-text="Image of paste the authorization token":::

#### 3. Setting up the Viva Goals app on the Jira side

- Go to “Apps” on the top menu bar and you'll see the “Viva Goals OKRs” app installed, select the app.

- In the next screen → paste the token you've copied to the clipboard from the previous step to the field where it says “Enter the Viva Goals Token” and select **Connect**, a “Successfully Connected to Viva Goals OKRs ” message should appear with a green tick or an “Error message” with a red tick will appear. If the second message appears, please contact support@ally.io for further assistance.

- In the second section of the setup, enter the email ID of the admin (on both Viva Goals and Jira sides) and select **Save**.

> [!NOTE]
> Make sure that the user setting up the connection is an Admin on both Jira as well as Viva Goals.

## Enabling Viva Goals in Jira

1. Once the app is authenticated successfully, you'll be able to see the Viva Goals component right within all your Jira epics, tasks, and issues.

    :::image type="content" source="../media/goals/goals-viva-goals-jira-component.png" alt-text="Image of Viva Goals component":::

2. . Select the Viva Goals component to create an Viva Goals project for the Jira issue. The project name is pre-populated based on the Jira issue and is editable. You can also edit the project level (individual, team, organization), the progress type, time period, and project owner. The time period and project owner are set by default based on the issue’s due date and the logged-in user. Select **Save** to create the project in Viva Goals. 

3. You’ll see the project’s progress and status right inside the Viva Goals component in your Jira issue.  

    :::image type="content" source="../media/goals/goals--project-progress-and-status.png" alt-text="Image of project progress and status":::

4. All the existing Jira issues (tasks, stories, bugs) will be listed in Viva Goals as project tasks. The project’s progress and subsequently the objective’s progress will automatically get updated when an issue is updated in Jira. 

    :::image type="content" source="../media/goals/goals-objective-progress.png" alt-text="Image of objective’s progress":::

## Actions supported by Viva Goals in Jira 

- **Add Alignment** 

    The project can be aligned to an OKR at any level. Clicking on this will take you to the alignment picker in Viva Goals, once you have updated it you can see the alignment against the project in JIRA. You can choose to multi-align the project. 

- **Edit Project** 

    You can edit the project details by clicking the ‘Edit project’ option. This will take you to the quick view in Viva Goals, where you’ll be able to edit the project details such as title, level, owner, time period.  

- **Unlink project from Viva Goals**

    Unlinking will ensure that the project created in Viva Goals will be unlinked from the Jira issue, any updates made to the issue or connected issues will not be represented on  Viva Goals. Select **Unlink project from Viva Goals**, and select the **Unlink project from Viva Goals** button.  

- **Unlink and delete project from Viva Goals**

    This will unlink the Jira issue and delete the Viva Goals project. Select **Unlink and delete project from Viva Goals**, and select the **Unlink & delete project** button.

    > [!NOTE]
    > If you're interested to set up the Viva Goals OKRs app for Jira, please drop an email to support@ally.io
    
Learn more about Viva Goals’ other integrations [here](https://help.ally.io/en/collections/30526-integrations). 