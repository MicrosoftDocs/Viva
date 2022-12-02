---
title: "Deeplinking into Viva Engage"
description: "Create deeplinks into Viva Engage"
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
# Deeplinking into Viva Engage

## Set up deeplinks into Viva Engage

Often times, you will want to create a deeplink to the Viva Engage app in Microsoft Teams or an entity within Viva Engage, such as a community. For example, you want to include a link to a conversation a leader shared, a community that you are launching, or a campaign you are emailing about.

This article will discuss how you can manually construct a deeplink into the Viva Engage app.

## Deeplink to the Viva Engage store entry
The following hyperlinks will open the Viva Engage store page in Microsoft Teams.

``` 
https://aka.ms/VivaEngage/Install
https://teams.microsoft.com/l/app/db5e5970-212f-477f-a3fc-2227dc7782bf
```

## Deeplink to Viva Engage directly
The following hyperlinks will directly open Viva Engage in Microsoft Teams. If the app is not installed, the user will be prompted to do so.

```
https://aka.ms/VivaEngage/Launch
https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage
```
## Deeplink to a sub-entity

First, 

`https://aka.ms/VivaEngage/Launch?context=%7B%22subEntityId%22:%22type=custom,data=`**`Campaign`**`:`**`eyJfdHlwZSI6IkNhbXBhaWduIiwiaWQiOiIyMDE2NDU4MzU1NzY5MzQ0In0`**`%22%7D


> https://aka.ms/VivaEngage/Launch?context=%7B%22subEntityId%22:%22type=custom,data=\\**Campaign\** : **eyJfdHlwZSI6IkNhbXBhaWduIiwiaWQiOiIyMDE2NDU4MzU1NzY5MzQ0In0**%22%7D
```
https://teams.microsoft.com/l/entity/db5e5970-212f-477f-a3fc-2227dc7782bf/vivaengage
```

