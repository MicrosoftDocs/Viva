---
ms.date: 02/12/2024
title: "Deep linking into Viva Engage"
description: "Create deep links into Viva Engage"
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---
# Deep linking into Viva Engage

Often, you'll want to create a deep link to the Viva Engage app in Microsoft Teams or an entity within Viva Engage, such as a community. For example, you want to include a link to a conversation that a leader shared, a community that you're launching, or a campaign you're emailing about.

This article discusses how to manually construct different deep links into the Viva Engage app.

> [!TIP]
> While the `https://aka.ms/...` link is shorter, we recommend the longer `https://teams.microsoft.com...` link if you're sharing the deep link in Teams. This way, you link directly to the Viva Engage tab without opening a new browser window.

## Deep link to the Viva Engage store entry

The following links open the Viva Engage store page in Microsoft Teams:

- <https://aka.ms/VivaEngage/Install>

- <https://teams.microsoft.com/l/app/db5e5970-212f-477f-a3fc-2227dc7782bf>

## Deep link to Viva Engage directly

The following links open Viva Engage in a browser and engage.cloud.microsoft, respectively. If the user has the Viva Engage mobile app installed, the links open the Viva Engage app.

- <https://aka.ms/VivaEngage/Web>

- <https://aka.ms/VivaEngage/Yammer>

The following links directly open Viva Engage in Microsoft Teams. If the app isn't installed, the user will be prompted to do so.

- <https://aka.ms/VivaEngage/Launch>

- <https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage>

The following link directly opens Viva Engage in Outlook, if available:

- <https://aka.ms/VivaEngage/Outlook>

## Deep link to Answers in Viva

To directly open Viva Engage in Teams to the Answers in Viva page, use one of the following links:

- <https://aka.ms/AnswersInViva>

- <https://aka.ms/VivaEngage/Answers>

- <https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage?context=%7B%22subEntityId%22%3A%22type%3Dcustom%2Cdata%3Dquestionspage%3A_%22%7D>


## Deep link to Leadership corner

In the browser (engage.cloud.microsoft) or the mobile app:

- <https://aka.ms/LeadershipCorner>

- <https://engage.cloud.microsoft/main/leadership-corner>

In Teams:

- <https://aka.ms/VivaEngage/LeadershipCorner>

- <https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage?context=%7B%22subEntityId%22:%22type=custom,data=leadershipcorner:null%22%7D> 

## Deep link to a Viva Engage entity

Links in these formats open the entity in Viva Engage in Teams.

- `https://aka.ms/VivaEngage/Launch?context=%7B%22subEntityId%22:%22type=custom,data=<EntityType>:<EntityId>%22%7D`
- `https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage?context=%7B%22subEntityId%22:%22type=custom,data=<EntityType>:<EntityId>%22%7D`

However, you also need to:

1. Replace _`<EntityType>`_ with one of the following values: 
   
   | Type      | Replace _`<EntityType>`_ with... |
   | --------- | ------------- |
   | Post      | `thread`  |
   | Community | `group`  |
   | Storyline | `user`  |
   | Campaign  | `campaign`  |

2. Fill in the  _`<EntityId>`_. The easiest way is to go to the corresponding page on **engage.cloud.microsoft** and paste the last part of the URL. 

For example, for the storyline of `https://engage.cloud.microsoft/main/users/eyJfdHlwZSI6IlVzZXIiLCJpZCI6IjUwMzIxMDg3kyOCJ9`, 
replace _`<EntityId>`_  with `eyJfdHlwZSI6IlVzZXIiLCJpZCI6IjUwMzIxMDg3kyOCJ9`.

> [!IMPORTANT] 
> Don't omit the `%22%7D` at the end of the URLs.
