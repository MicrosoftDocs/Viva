---
ms.date: 06/16/2023
title: Customize Viva Insights privacy settings
description: Learn how to customize  Viva Insights privacy settings in the advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Customize Viva Insights privacy settings

![insights admin](../images/applies-to-insights-admin.png) *Applies to: Insights Administrator*

:::image type="content" source="../images/setup-vi-settings.png" alt-text="Image alt text." lightbox="../images/setup-vi-settings.png":::

To get the most out of the Viva Insights experience, you might want to set up a few optional controls in the **Privacy settings** page. 

## Minimum group size

Set the minimum group size, which is the minimum aggregation threshold for insights. In other words, this is the smallest number of people that Viva Insights considers a “group.” Viva Insights shows insights about groups in the app in Teams and on the web, in organization insights throughout the app. You should set this number to at least 10.

## Keyword suppression

Specify sensitive keywords that might appear in email subject lines or meeting titles across your organization. After you set them, subject lines or meeting titles that contain these keywords won't appear in any surface that uses Viva Insights data, including query output.

We show you how to use this feature in [Keyword suppression](../admin/keyword-suppression.md).

## End-user opt-out

The **End-user opt-out** control lets users choose whether their metrics—which are always de-identified—appear in [person query](..//analyst/person-query-overview.md) results. Analysts run person queries through the advanced insights app. When users opt out, future person queries and those that refresh each week are affected. Opt-out doesn’t apply to aggregated insights (like organization insights) and query results from collaboration events (like meetings). 

Users can find opt-out settings in their Viva Insights app in Teams or on the web under **Settings > Privacy**. After you turn on the **End-user opt-out** control, users who already opted out of Viva Insights through their app in Teams or on the web are automatically opted out of person query data. Settings take effect after one day. Users can opt back in to Viva Insights whenever they want and they’ll see their previously saved settings. 

## Save changes

After you’re done making changes to group size and/or opt-out settings, select **Save changes**.

:::image type="content" source="../images/privacy-settings10-small.png" alt-text="Screenshot that shows the Manager settings page." lightbox="../images/privacy-settings10.png":::

## Next steps

> [!div class="nextstepaction"]
> [Upload organizational data](upload-data.md)

*Applies to: Insights Administrator*


