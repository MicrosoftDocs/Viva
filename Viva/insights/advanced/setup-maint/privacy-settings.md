---
ms.date: 01/08/2024
title: Customize Viva Insights privacy settings
description: Learn how to customize  Viva Insights privacy settings in the advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: ablubetk
audience: Admin
---

# Customize Viva Insights privacy settings

![insights admin](../images/applies-to-insights-admin.png) *Applies to: Insights Administrator*

:::image type="content" source="../images/setup-vi-settings-1.png" alt-text="Image alt text." lightbox="../images/setup-vi-settings-1.png":::

To get the most out of the Viva Insights experience, you might want to set up a few optional controls in the **Privacy settings** page.

## Partitions

Partitions are analyst workspaces that include only certain employee data and attributes. If you turn on partitions, going forward, all analysts assigned to Viva Insights must be manually assigned a partition to access the Viva Insights dataset. Existing analysts, however, will continue to have access to full tenant data through the global partition. 

Once you turn on partitions, you can’t turn them off without contacting us. 

:::image type="content" source="../images/admin-partitions-turn-on.png" alt-text="Screenshot that shows the option to turn on partitions in privacy settings." lightbox="../images/admin-partitions-turn-on.png":::

[Learn more about partitions and how to set them up](../admin/partitions.md).

## Domain reclassification

Reclassifying domains in Viva Insights classifies external domains as internal. You might reclassify external domains for a few reasons: maybe your company recently acquired or merged with another company, and formerly external employees are now internal. Or, your company has subsidiaries, and you want to make sure collaboration with those domains is considered internal.

To reclassify domains, go to the **Reclassify external domains** section. From the dropdown menu, select the external domains you want to classify as internal.

>[!Important]
>Changes to these settings take effect after the next data refresh, which might take up to one week. 


## Minimum group size

Set the minimum group size, which is the minimum aggregation threshold for insights. In other words, this is the smallest number of people that Viva Insights considers a “group.” Viva Insights shows insights about groups in the app in Teams and on the web, in organization insights throughout the app. You'll need to set this number to at least 10.

To learn how team and group size differ, refer to [What’s the difference between minimum team size and minimum group size?](manager-settings.md#whats-the-difference-between-minimum-team-size-and-minimum-group-size).

## Keyword suppression

Specify sensitive keywords that might appear in email subject lines or meeting titles across your organization. After you set them, subject lines or meeting titles that contain these keywords won't appear in any surface that uses Viva Insights data, including query output.

We show you how to use this feature in [Keyword suppression](../admin/keyword-suppression.md).

## Domain suppression

Prevent data associated with people in sensitive domains from showing in analyst experiences. We show you how to use this feature in [Domain suppression](../admin/domain-suppression.md).

>[!Important]
>Changes to these settings take effect after the next data refresh, which might take up to one week. 




## End-user opt-out

Users can always [opt out of personal insights](https://support.microsoft.com/topic/opt-out-of-viva-insights-ecfd76f9-52ef-4882-9235-be1f59c25967). In addition to this opt-out feature, we also built the **End-user opt-out** control. With this control, you let users choose whether their metrics—which are always de-identified—appear in [person query](../analyst/person-query-overview.md) results. Analysts run person queries through the advanced insights app. When users opt out, future person queries and those that refresh each week are affected. Opt-out doesn’t apply to aggregated insights (like organization insights) and query results from collaboration events (like meetings). 

Users can find opt-out settings in their Viva Insights app in Teams or on the web under **Settings > Privacy**. After you turn on the **End-user opt-out** control, users who already opted out of Viva Insights through their app in Teams or on the web are automatically opted out of person query data. Settings take effect after one day. Users can opt back in to Viva Insights whenever they want and they’ll see their previously saved settings. 

## Save changes

After you’re done making changes to group size and/or opt-out settings, select **Save changes**.

:::image type="content" source="../images/privacy-settings10-small.png" alt-text="Screenshot that shows the Manager settings page." lightbox="../images/privacy-settings10.png":::

## Next steps

> [!div class="nextstepaction"]
> [Upload organizational data](upload-data.md)

*Applies to: Insights Administrator*


