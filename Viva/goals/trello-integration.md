---
ms.date: 04/03/2024
title: Trello integration
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- vg-integration
search.appverid:
- MET150
description: "Learn how to integrate Trello with your key results."
---

# Trello integration

Viva Goals can integrate with Trello board to automatically update key results in Viva Goals. For example, let's say you're a marketer who uses a Trello board to keep track of blog posts you want to publish. Integrating with Trello would let you easily keep track of which posts have been completed from within Viva Goals.

## Set up a Trello integration

If you're an admin, follow these steps to set up a Trello integration in Viva Goals:

1. Go to the Viva Goals integrations page:  **Admin** > **Integrations**.

1. Find Trello under the **Data Integrations** section, or use the search function to locate it.

    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::

1. Next to Trello, select **Enable**. Note that if a Trello integration has already been enabled, the button will say **Manage** instead of **Enable**.

1. Select **New Connection**. In the dialog that follows, sign in to your Trello account. Next, configure Trello connections to link to your key results to update progress.

     :::image type="content" source="../media/goals/8/trello-configure-new-connection.png" alt-text="Screenshot shows where you enter a name for your new Trello connection." lightbox="../media/goals/8/trello-configure-new-connection.png":::

     :::image type="content" source="../media/goals/8/trello-sign-in.png" alt-text="Screenshot that shows the Connect to Trello dialog with an option to sign in to Trello." lightbox="../media/goals/8/trello-sign-in.png":::

     :::image type="content" source="../media/goals/8/trello-connect-to.png" alt-text="Screenshot that shows the Connect to Trello dialog with connection options filled out." lightbox="../media/goals/8/trello-connect-to.png":::

1. Select **Next** to finish setup.

Viva Goals lets you connect with multiple Trello accounts. Select **New Connection** to add another connection. The connections are differentiated by name. These names are displayed to users when they link their key results to Trello boards.

## Link a key result to a Trello board

Once setup is complete, users in your organization can link their key results to Trello boards.

1. When you create (or edit) a key result, the **Progress and Status** dropdown will have a section with the text "Connect to a data source for automatic progress updates". Search for and select the **Trello** icon from the list of integrations.

    :::image type="content" source="../media/goals/8/trello-datasource.png" alt-text="Screenshot shows where you select Trello as the data source in Viva goals." lightbox="../media/goals/8/trello-datasource.png":::

1. If you already created a Trello connection or had one shared with you by an administrator in your organization, that connection will be automatically selected for you. If you don't have access to any existing connections, Viva Goals will prompt you to add a new connection.

1. After you select or add a connection, select the Trello **Board** that has the cards data that you want to connect to a key result.

    :::image type="content" source="../media/goals/8/trello-connection-details.png" alt-text="Screenshot shows how you specify the Trello board and other details for your new connection." lightbox="../media/goals/8/trello-connection-details.png":::

1. After you select the Trello board, you can further filter the list of cards by selecting one or more of the following criteria:

    - Cards belonging to a specific list
    - Cards assigned to a specific owner
    - Cards with a specific label
    - Cards with a specific completion status

    For example, let's say you want to use the number of blogs completed as a key performance indicator (KPI) in Viva Goals. If there are completed blog post cards in the **Finished** column of your Trello board, you can select **Finished** from the list of options in the **Board List** dropdown.

    If you have the completed blogs marked as *labels* in Trello instead, you can select the label that you use to mark cards as completed from the **Labels** dropdown. You can also use labels to filter specific cards that belong to a category or subcategory.

    You can also filter based on completion status. You can filter cards that have due dates and that are marked as completed or not completed. To select cards with any status, choose **Any**.

    **% Completed versus KPI**

    Viva Goals will track progress based on whether the objective was measured by KPI or percent complete. For KPI-based objectives, progress will be computed based on the number of cards that match your filters and the configuration. An objective like **Complete 10 blog posts** falls into this category.

    For percent complete-based objectives, Viva Goals will compute the progress based on the percentage of cards that have a **Completed** status out of the total number of cards that match the filters and the configuration. In this case, a good example would be if you had a board with a list of cards that map to an initiative, and you wanted to measure the progress of the initiative over time.

1. Select **Next** to finalize and save your key result. You should now see a Trello icon in your key result's **Last updated** column. The key result syncs automatically every hour. To refresh it manually, select the Trello icon and choose **Sync**.
