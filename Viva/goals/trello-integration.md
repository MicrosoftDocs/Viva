---
title: "Trello Integration"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager:
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to use the Trello integration with your OKRs."
---

# Trello integration

Viva Goals can integrate with boards in Trello to automatically update your objectives and key results (OKRs) in Viva Goals. 
    
Let's consider this example: You're a marketer who uses a Trello board to keep track of blog posts you want to publish. Use can use Trello integration to easily keep track of completed posts. Viva Goals will sync the values for you and chart your progress toward your OKR, saving time while keeping your OKRs current.

## How to set up Trello integration

An admin follows these steps to set up the Trello integration in Viva Goals: 

1. Go to Viva Goals integrations page:  **Admin** -> **Integrations**.
    
    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::

2. **Enable** Trello integration.
    
    :::image type="content" source="../media/goals/8/trello-enable-button.png" alt-text="Screenshot shows where you enable Trello in Viva Goals." lightbox="../media/goals/8/trello-enable-button.png":::

3. Select **New Connection**. In the dialog that follows, sign in to your Trello account. Next, configure Trello connections to link to your OKRs to update progress.
    
     :::image type="content" source="../media/goals/8/trello-configure-new-connection.png" alt-text="Screenshot shows where you enter a name for your new Trello connection." lightbox="../media/goals/8/trello-configure-new-connection.png":::

4. Select **Next** to finish setup.

Viva Goals lets you connect with multiple Trello accounts. Select **New connection** to add another connection. The connections are differentiated by name. These names are displayed to users when they link their OKRs to Trello boards.

## How to use Trello integration

After setup is complete, users in your organization can link their OKRs to Trello boards.

1. When you create (or edit) an objective or key result, select **Connect data source to auto-update progress**.

2. From the list of integrations, choose **Trello**.
    
    :::image type="content" source="../media/goals/8/trello-datasource.png" alt-text="Screenshot shows where you select Trello as the data source in Viva goals." lightbox="../media/goals/8/trello-datasource.png":::

3. If you already created a Trello connection or an administrator in your organization shared a Trello connection with you, that connection will be automatically selected for you. If there are no connections already created or shared, Viva Goals will prompt you to add a new connection.

4. After you select or add a connection, select the Trello **Board** that has the cards data that you want to connect to an OKR.
    
    :::image type="content" source="../media/goals/8/trello-connection-details.png" alt-text="Screenshot shows how you specify the Trello board and other details for your new connection." lightbox="../media/goals/8/trello-connection-details.png":::

5. After you select the Trello board, you can further filter the list of cards by selecting one or more of the following criteria:

    - Cards belonging to a specific list
    - Cards assigned to a specific owner
    - Cards with a specific label
    - Cards with a specific completion status

    For example, say you want to measure the number of blogs completed as a key performance indicator (KPI) in Viva Goals. If there are completed blog post cards in the **Finished** column of your Trello board, you can select **Finished** from the list of options in the **Board List** dropdown.

    If you have the completed blogs marked as *labels* in Trello instead, you can select the label that you use to mark cards as completed from the **Labels** dropdown. You can also use labels to filter specific cards that belong to a category or subcategory.

    You can also filter based on completion status. You can filter cards that have due dates and that are marked as completed or not completed. To select cards with any status, choose **Any**.

    **% Completed versus KPI**

    Viva Goals will track progress based on whether the objective was measured by KPI or percent complete. For KPI-based objectives, progress will be computed based on the number of cards that match your filters and the configuration. An objective like **Complete 10 blog posts** falls into this category.

    For percent complete-based objectives, Viva Goals will compute the progress based on the percentage of cards that have a **Completed** status to the total number of cards that match the filters and the configuration. In this case, a good example is a board with a list of cards that maps to a project, and you want to measure the progress of the project over time.

6. Select **Next** to finish and save your OKR. You should now see a Trello icon next to the OKR/ Viva Goals will now automatically count up the finished blog posts. The OKR syncs automatically every hour. To  refresh it manually, select **refresh**. 
    