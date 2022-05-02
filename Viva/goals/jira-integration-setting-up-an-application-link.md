---
title: Jira integration - setting up an application link
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

description: "Instructions on how to configure the application link inside Jira to enable Viva Goals <> Jira integration."
---

# Jira integration - setting up an application link

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Creating an application link inside Jira is required for enabling users in your Viva Goals organization to easily connect to Jira. This will help users to automatically track their objectives inside Viva Goals based on the progress made in Jira. 


To create an Application Link from a self-managed (on-premise) Jira instance,

1. In Jira, navigate to **Jira settings (cog icon) > Applications > Application links**.

    :::image type="content" source="../media/goals/goals-create-application-link.png" alt-text="Image of create an application link":::

2. In the Enter the URL of the application you want to link field, enter https://app.ally.io and then select **Create new link**. Ignore the No response was received from the URL you entered warning that is displayed and select **Continue**.

    :::image type="content" source="../media/goals/goals-url.png" alt-text="Image of Enter the URL"::: 

3. On the first screen of the Link applications dialog, select the **Create incoming link checkbox (1)**.

    :::image type="content" source="../media/goals/goals-link-applications.png" alt-text="Image of link application":::

    It doesn't matter what you enter in the remaining fields (URL, name, type, and so on). This is because we only want to retrieve data from Jira, therefore we only need to set up a one-way (incoming) link from the client to Jira.

4. On the next screen of the Link applications dialog, enter the consumer and public key details for the Viva Goals client. You can get the consumer key and the public key information that goes into this step from [here](https://www.ally.io/uploads/jira-public-keys/).

    :::image type="content" source="../media/goals/goals-link-applications-public-key.png" alt-text="Image of link applications public key":::

5. Select **Continue**. The application link you created will show in a screen like the following.

    :::image type="content" source="../media/goals/goals-link-applications-link-created.png" alt-text="Image of application link created":::

You're all setup! Users in your organization can now connect to their Jira account and [create a Jira connection](https://help.ally.io/en/articles/2285939-jira-integration) inside Viva Goals. Integrating Jira with Viva Goals allows any updates on linked Jira user-stories or Epics to automatically track progress on Viva Goals OKRs. 