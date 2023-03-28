---
ms.date: 03/28/2023
title: "Zapier Integration"
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
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Connect Viva Goals to all the tools you love with the new Zapier integration."
---

# Zapier integration

Viva Goals integration with Zapier enables you to connect Viva Goals with all the tools you use every day. Say, for instance, you have an OKR to 'Preview mobile app with 5 enterprise customers', you can directly link this objective with a Trello card where you're tracking your thought Beta Customers, so with every checklist item update, a check-in is made automatically to the OKR in Viva Goals.

## Setting up  

How to connect an app of your choice with Viva Goals:

1. Navigate to https://zapier.com/app/zaps and sign-in.
1. Select on **Create Zap** and start by selecting an app for the Zap’s trigger. Go on to choose the app’s trigger event and connect with Trello as we're tracking Beta customers for our mobile app as a checklist in Trello. Once you’re done setting up your trigger, select on **Continue** to set up the action.
    :::image type="content" source="../media/goals/zapier-integration/new-trello.png" alt-text="Screenshot of setting up a new trigger." lightbox="../media/goals/zapier-integration/new-trello.png":::
1. When you’re setting up your Zap’s action, select Microsoft Viva Goals from the **App & Event** dropdown. Select **Create a Check-in** from the Event and select on **Continue**.
    :::image type="content" source="../media/goals/zapier-integration/vg.png" alt-text="Screenshot of setting up the zaps actions." lightbox="../media/goals/zapier-integration/vg.png":::
1. Select on the **Connect to New Account** option. You'll then be prompted to connect to a Viva Goals account.
    :::image type="content" source="../media/goals/zapier-integration/connect.png" alt-text="Screenshot of connecting to a new account." lightbox="../media/goals/zapier-integration/connect.png":::
1. You should then get a pop-up window from Viva Goals asking you to sign-in to authorize the connection between your Viva Goals account and Zapier.  
    :::image type="content" source="../media/goals/zapier-integration/scope.png" alt-text="Screenshot of the permissions request to connect with Viva Goals." lightbox="../media/goals/zapier-integration/scope.png":::
1. After logging in, you'll get sent back to your zap where you now have your Viva Goals account connected.
1. Choose the Key Result to which you want to connect, select the metric’s progress that should be tracked to make check-ins, and add additional notes or comments if any.
    :::image type="content" source="../media/goals/zapier-integration/full.png" alt-text="Screenshot of a completely filled out Zap." lightbox="../media/goals/zapier-integration/full.png":::
1. Set up the rest of your Zap and turn it on, once done.

Now when viewing the connected key results in Viva Goals, you'll see an icon next to the progress bar, and be able to see the activity updates from Zapier in the activity section.

:::image type="content" source="../media/goals/zapier-integration/success.png" alt-text="Screenshot of a connected zap in Viva Goals." lightbox="../media/goals/zapier-integration/success.png":::

:::image type="content" source="../media/goals/zapier-integration/activity.png" alt-text="Screenshot of Zapier activity showing in Viva Goals." lightbox="../media/goals/zapier-integration/activity.png":::

## FAQs (Frequently Asked Questions)

1. **Managing the Viva Goals - Zapier Integration**
    1. You'll be able to edit, pause, disable the integration from your Zapier account. 

2. **Can I connect Initiatives in Viva Goals with Zapier?**
    1. Currently, Viva Goals supports integration with key results. 

3. **What metrics can Viva Goals pull from Zapier?**
    1. The current check-in metric can be pulled from Zapier, which can track the KR progress.

4. **Why isn't my data syncing instantly after making a connection with Zapier?**
    1. Some Zaps aren't instant, and sync will happen based on the Zaps periodic sync time. 

5. **Can I make a manual check-in on Zapier integrated OKRs?**
    1. Yes, users can make manual check-ins and also stop Zapier integration by selecting the 'Stop updating automatically from Zapier' option.
    
6. **Can I connect with another integration after connecting an OKR with Zapier?**
    1. You'll have to remove the Zapier integration and readd any integration of your choice. 

7. **How can I remove the Zapier integration from Viva Goals?**
    1. Select on the **Edit** objective and head over to the **Progress** section.  
    1. Select the **Connected to Zapier** dropdown and select on **Remove** from the popup that appears.
         :::image type="content" source="../media/goals/zapier-integration/remove.png" alt-text="Screenshot of removing the Zapier integration from a key result" lightbox="../media/goals/zapier-integration/remove.png":::