---
title: "Deep linking into Viva Engage"
description: "Create deep links into Viva Engage"
ms.reviewer: ethli
ms.author: v-jebizie
author: v-jebizie
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---
# Deep linking into Viva Engage

## Set up deep links into Viva Engage

Often, you'll want to create a deep link to the Viva Engage app in Microsoft Teams or an entity within Viva Engage, such as a community. For example, you want to include a link to a conversation a leader shared, a community that you are launching, or a campaign you are emailing about.

This article will discuss how you can manually construct a deep link into the Viva Engage app.

## Deep link to the Viva Engage store entry
The following links open the Viva Engage store page in Microsoft Teams:
- https://aka.ms/VivaEngage/Install
- https://teams.microsoft.com/l/app/db5e5970-212f-477f-a3fc-2227dc7782bf

## Deep link to Viva Engage directly
The following links directly open Viva Engage in Microsoft Teams. If the app isn't installed, the user will be prompted to do so.
- https://aka.ms/VivaEngage/Launch
- https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage


## Deep link to a Viva Engage entity
Similarly these links will open the entity in Viva Engage in Teams. 

- `https://aka.ms/VivaEngage/Launch?context=%7B%22subEntityId%22:%22type=custom,data=\<entityType\>:\<entityId\>%22%7D`
- `https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage?context=%7B%22subEntityId%22:%22type=custom,data=\<entityType\>:\<entityId\>%22%7D`

However, you will need to:
- replace _`<entityType>`_ with one of the following:
| Type      | Replace _`<entityType>`_ with... |
| --------- | ------------- |
| Post      | `threaad`  |
| Community | `group`  |
| Campaign  | `campaign`  |
| Storyline | `user`  |
| Leadership corner | `leadershipcorner`  |
  
- and fill in the  _`<entityid>`_. The easiest way is by going to the corresponding page on Yammer.com, and then pasting the last part of the URL. For example, for the storyline of 'https://web.yammer.com/main/users/eyJfdHlwZSI6IlVzZXIiLCJpZCI6IjUwMzIxMDg3kyOCJ9`, _`<entityid>`_ replace with eyJfdHlwZSI6IlVzZXIiLCJpZCI6IjUwMzIxMDg3kyOCJ9
