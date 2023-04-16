---
ms.date: 07/15/2022
title: Microsoft Viva Insights setup
description: Learn what's required to set up Microsoft Viva Insights 
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

# Set up advanced insights


## Required settings

### Verify licenses and roles 

Make sure your Microsoft 365 admin has assigned licenses and roles to people in your organization. For more information about this process, refer to [Assign licenses](assign-licenses.md) and [Assign roles](assign-user-roles.md). To learn about Viva Insights licenses and other related requirements, refer to [Environment requirements](environment-requirements.md).

>[!Important]
>At least 10 people in your organization need to have Viva Insights licenses assigned to them before analysts can start using the advanced insights app. You can only assign Viva Insights licenses to current Microsoft 365 license holders.
>
>After you assign licenses, give Viva Insights five days to process collaboration data. After those five days are up, your organization is ready to start running queries.

After licenses and roles are assigned—and after the app successfully processes organizational data from Azure Active Directory (AD)—you’ve fulfilled all setup requirements. 

## Optional settings

To get the most out of the Viva Insights experience, you might want to set up a few optional controls. 

>[!Note]
>The **Insights Administrator** role is required to perform the following tasks.

### Customize privacy settings

#### Minimum group size

Set the minimum group size, which is the minimum aggregation threshold for insights. In other words, this is the smallest number of people that Viva Insights considers a “group.” Viva Insights shows insights about groups in the app in Teams and on the web, in organization insights throughout the app. You should set this number to at least 10.

#### End-user opt-out

The **End-user opt-out** control lets users choose whether their metrics—which are always de-identified—appear in [person query](..//analyst/person-query-overview.md) results. Analysts run person queries through the advanced insights app. When users opt out, future person queries and those that refresh each week are affected. Opt-out doesn’t apply to aggregated insights (like organization insights) and query results from collaboration events (like meetings). 

Users can find opt-out settings in their Viva Insights app in Teams or on the web under **Settings > Privacy**. After you turn on the **End-user opt-out** control, users who already opted out of Viva Insights through their app in Teams or on the web are automatically opted out of person query data. Settings take effect after one day. Users can opt back in to Viva Insights whenever they want and they’ll see their previously saved settings. 

#### Save changes

After you’re done making changes to group size and/or opt-out settings, select **Save changes**.

:::image type="content" source="../images/privacy-settings10-small.png" alt-text="Screenshot that shows the Manager settings page." lightbox="../images/privacy-settings10.png":::

## Customize manager settings 

Use the **Manager settings** page to allow managers to see aggregated collaboration insights. These insights appear in the Viva Insights app in Teams or on the web. Learn more about manager settings in [Manager settings](manager-settings.md). 

### Prepare and upload organizational data 

By default, Viva Insights uses your organization’s Azure AD data. This data automatically feeds into Viva Insights, so you don’t need to do anything extra to set up organizational data in the advanced insights app. If you want to upload your organizational data as a .csv file instead of using Azure AD, follow the guidance in [Prepare organizational data](../admin/prepare-org-data.md) and [Upload organizational data (first upload)](../admin/upload-org-data-first.md). After you upload a file, here’s the basic process:

1. Data mapping – You map the uploaded data to the applicable field names. For details, refer to [Field mapping](../admin/upload-org-data-first.md#field-mapping).
1. Data validation – Viva Insights validates the data. When validation completes successfully, you'll see a confirmation message. If validation wasn’t successful, you’re  advised what to do next. For details, refer to [Validation](../admin/upload-org-data-first.md#validation).
1. Data processing – Viva Insights processes the validated data. When the processing is done, you'll see a message that setup is complete.

## Related topics

[Manager settings](manager-settings.md)

[Prepare organizational data](../admin/prepare-org-data.md)

[Upload organizational data (first upload)](../admin/upload-org-data-first.md)
