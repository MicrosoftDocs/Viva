---
title: "Trello Integration"
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

description: "Learn how to use the Trello integration with your OKRs."
---

# Trello integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals can integrate with boards in Trello to automatically update your Objectives and Key Results (OKRs) inside Viva Goals. 
    
Let's take this example: you are a marketer using a Trello board to keep track of the blog posts you want to publish. Use the Trello integration to easily keep track of completed posts. Viva Goals will sync the values for you and chart your progress toward your OKR, saving time while keeping OKRs current.

## How to set up the Trello integration

An admin can set up the Trello integration on Viva Goals. Take these steps: 

1. Navigate to Viva Goals’ integrations page through **Admin -> Integrations**.
    
    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::

2. **Enable** the Trello integration.
    
    :::image type="content" source="../media/goals/8/trello-enable-button-in-viva-goals.png" alt-text="Enabling Trello in Viva Goals." lightbox="../media/goals/8/trello-enable-button-in-viva-goals.png":::

3. Select **New Connection** and in the popup that follows, sign into your Trello account. Next, configure Trello connections that can be used by Viva Goals users to link their OKRs and update progress.
    
     :::image type="content" source="../media/goals/8/trello-creating-new-connection-in-viva-goals.png" alt-text="Configuring new Trello connection in Viva Goals." lightbox="../media/goals/8/trello-creating-new-connection-in-viva-goals.png":::

4. Select **Next** to finish the setup

Viva Goals allows you to connect with multiple Trello accounts. Select **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to Trello boards.

## How to use the Trello Integration

Once the setup is complete, users in your organization can link their OKRs to Trello boards.

1. While creating (or editing) an Objective or Key Result, select **Connect data source to auto-update progress**.

2. From the list of integrations, pick Trello.
    
    :::image type="content" source="../media/goals/8/trello-datasource-from-list-of-integrations-in-viva-goals.png" alt-text="Selecting Trello from the list of data sources in Viva goals." lightbox="../media/goals/8/trello-datasource-from-list-of-integrations-in-viva-goals.png":::

3. If you already created a Trello connection or an administrator in your organization shared a Trello connection with you, that will be automatically selected for you. If there are no connections created or shared already, Viva Goals will prompt you to add a new connection.

4. Once the connection is selected, select the Trello **Board** that has the cards data that you wish to connect to an OKR.
    
    :::image type="content" source="../media/goals/8/trello-connection-details-in-viva-goals.png" alt-text="Adding new Trello connection to OKRs in Viva goals." lightbox="../media/goals/8/trello-connection-details-in-viva-goals.png":::

5. After you've selected the Trello Board, you can further filter the list of cards by selecting one or more of the following criteria:

    a. Cards belonging to a specific list.

    b. Cards assigned to a specific Owner.

    c. Cards with a specific label.

    d. Card with specific completion status.

    For example, if you want to measure the number of blogs completed as a key performance indicator (KPI) inside Viva Goals and if you have completed blog post cards in your Trello board in the **Finished** column, you can select **Finished** from the list of options in the **Board List** dropdown.

    If you have the completed blogs marked as labels in Trello instead, you can select the label that you use to mark cards as completed from the **Labels** dropdown. Labels can also be used for filtering specific cards belonging to a category or subcategory.

    You can also filter based on Completion status. This will let you filter cards that have due dates and those marked as completed or cards that have due dates and aren't completed. To select all cards, choose **Any,** which will include cards of any status whether it has a due date or not.

    **% Completed vs KPI**

    Viva Goals will track progress based on whether the objective was selected to be measured as a KPI or Percent Complete. For KPI based objectives, the progress will be computed based on the number of cards matching your filters and the configuration. An objective like **Complete 10 blog posts** falls into this category.

    For percent complete based objectives, Viva Goals will compute the progress based on the percentage of cards that has a completion status as **Completed** to the total number of cards matching the filters and the configuration. In this case, a good example will be a board with a list of cards that maps to a project and you want to measure the ongoing progress of the project over time.

    In the following example, we're counting the number of completed blog posts:

6. Hit next to finish and save your OKR. You should now see a Trello icon next to the OKR - now Viva Goals will automatically count up the finished blog posts. The OKR syncs automatically every hour, but to refresh it manually you can select **refresh**.
