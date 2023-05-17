---
ms.date: 03/29/2023
title: Use the trend graph in a Viva Glint Employee Lifecycle program
ms.reviewer: 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "The Trend Graph for Employee Lifecycle surveys behaves differently than that of recurring survey programs."
---

# Use the trend graph in a Viva Glint Employee Lifecycle program

The Trend Graph for Employee Lifecycle (ELC) surveys behaves differently than that of a Microsoft Viva Glint recurring program. 

- By default, the scores displayed in reports are filtered to responses received in the last 90 days. 
- As ELC surveys are always active: Reports will group scores based on the date range selected or the default 90 days.  
- Responses appear on the dashboard as feedback is submitted. The manager will see responses on their dashboard after the program thresholds are met and according to their user profile permissions. 

## When the default period is used 

- The latest data point on the graph will be any surveys received within the past 90 days. 
- The next point will be the 90 days before the first data point (180 days - 91 days before today). 
- The point prior to that will be 90 days before the second data point (270 days - 181 days before today), and so on.  

The date that is displayed when you hover over data points is Day 1 of that range, meaning that *the most recent* data point is 90 days before today's date (the date being studied). This date is not capped by the actual survey launch date, so a date earlier than the survey launch date can be displayed on one of these data points. 

  > [!TIP]
  >**Example**: 
   > - Today's date is May 21, 2022. 
   > - The Exit survey launched on January 9, 2022. 
   > - The first data point on the trend graph shows February 21, 202 - 90 days before today's date. 
   > - The second data point on the trend graph shows November 23, 2021 - 180 days before today's date.   
 

   > [!NOTE]
   > The trend graph doesn't reference the actual survey launch date when determining the date to display. It uses 90-day intervals. In this scenario, no responses were received from November 23 - January 8th as the program did not open until January 9th.