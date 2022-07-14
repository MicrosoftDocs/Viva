---
title: Step 2-Create Dataverse tables
description: Learn how to create dataverse tables
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Step 2-Create Dataverse tables

1. Create the Dataverse tables that are described below. For more information on creating Dataverse tables, see [Create a custom table](/power-apps/maker/data-platform/data-platform-create-entity).

## Yume Cards

|Column |Description  |
|---------|---------|
|TitleId     |   **Whole number**: Unique ID for the Title and Suggestions      |
|TitleName     |    **Text (850)**: (Primary column, Option Required) Title for the main category (needed only for the title card)     |
|TitleType     |**Text (100)**: Defines what the TitleName will be used for;               **MainTitle**: Identify TitleName as the main card title; **ContentTitle**: Identify the TitleName as the title for the content. |
|TitleContent     |   **Text (2048)**: Content for the card      |
|ContentType     |   **Text (100)**: Defines what the TitleContent will be used for;               **MainTitle**: Identify the TitleContent as the Description content for the main card title; **ContentTitle**: Identify the TitleContent as the content of the main card.      |
|CardType     |     **Text (100)**: Identifies how the display area content for the card will be presented.            **Metrics**: Predefined Viva Personal Insights based on graph data; **Horizontal**: Left/right control for navigating the content for the main card; **Vertical**: Vertical gallery (list) display of the content.  |
|DisplayOrder     |     **Whole Number**: The order to display the content in the horizontal/vertical format.    |

## Yume Meeting Notes

|Column  |Description  |
|---------|---------|
|MeetingId     |    **Text (512)**: (Primary) Outlook meeting ID     |
|MeetingDateTime     |     Date and time    |
|MeetingName     | **Text (1024)**: Outlook meeting subject line        |
|MeetingTasks     |   **Text (2048)**: Delimited task list      |
|CaIds    |     **Text (1024)**: Delimited card IDs    |
|Emp Feedback     |    **Text(1024)**: Emp meeting feedback     |
|Emp Feeling     |      **Text(100)**: Emp meeting sentiment   |

## Yume User Options

|Column  |Description  |
|---------|---------|
|SettingName     |    **Text(100)**: (Primary) Setting Name     |
|SettingValue     |   **Text (512)**: Content for the card      |

2. During the Dataverses table creation, make a note of the table prefix name.

   :::image type="content" source="../media/tables-yume-card-data.png" alt-text="Tables containing Yume card data":::