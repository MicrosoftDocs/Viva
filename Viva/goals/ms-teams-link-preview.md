---
ms.date: 08/10/2023
title: Link Previews in Teams 
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Preview links from Viva Goals in Microsoft Teams."
---

# Link Previews in Microsoft Teams 

When you paste a link from Viva Goals (web app or teams app) into the Microsoft Teams message box, you see a link preview with relevant details about the item. This provides users with context around the goals they're working towards. Users can also update these goals by clicking **View Details** on the link without clicking away from the conversation and losing focus. 

Link previews are provided for the following items in Viva Goals: 

- OKR and Initiative lists 
- OKRs and Initiatives 
- Check-ins 
- Wins (celebrating check-ins) 
- Updates 

## How link previews work

### OKRs and Initiative lists

1. Navigate to the team or user in Viva Goals whose OKRs or Initiatives you want to share.
    1. If you are on Viva Goals in a web browser, copy the url from the browser address bar. 
    1. If you are in Teams, select **Share > Copy link**.
1. Head to your chat or channel of choice and paste the url. 
1. The link unfurls into a link preview.
    1. The OKRs or initiatives shown will correspond to the time period you were viewing when you copied the link. 
1. For a smoother experience where you don’t need to leave Viva Goals, you can select  **Share > Teams**. This opens a dialog box where you can specify the Teams chat or channel you want to share with and enter a message, all without leaving Viva Goals.

### OKRs and Initiatives 

To share an OKR or initiative, navigate to the specific OKR or initiative you want to share and select the **Share > Copy Link** and/or **Share > Teams** option.

### Check-ins and Wins

You can share a specific check-in, perhaps to ask questions about the progress made. Alternatively, you can “Share a win”, which will share the check-in with some celebratory text. Use this to motivate your team as they achieve goals. These options are available in the Share menu for a specific check-in. Currently, only manual check-ins are supported for sharing. Rollup and check-ins from integrations do not have a Share option.

### Updates

Your team might be using the **[Share an update](goals-broadcast.md)** feature to send updates about their overall progress. You can reshare these updates to Teams by clicking on the Updates tab where you find the Share options for Copy Link and Teams for each update.

## Viewing details from a link preview 

When you select **View Details** within the preview, you're taken to a **Stage View**. This is a focused experience directly in the chat or channel where you can work on the item from Viva Goals: either a list or a specific item, check-in or update. This lets you update progress or edit the item directly in your flow of work.

Should you need to see more details, you can use the options to **Open in App**, which will open the Viva Goals app in Teams, or **Open in Web** from the stage view, to open the web version of Viva Goals.

## Link previews and privacy 

If an OKR is marked as private, Viva Goals won't show a link preview. This is to prevent accidental exposure of private Viva Goals content. Similarly, if private OKRs are part of a list that is being previewed, they won't be shown, or counted in the list of items.  

## Disabling Share to Teams and Share a Win options 

Some tenants might not use MS Teams as their collaboration app of choice. In such cases, admins might want to disable these menu options, so that they don't show up under **Share** in the Viva Goals UI. You can disable these options from the Viva Goals Admin Portal, under Sharing permissions.