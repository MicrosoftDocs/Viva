---
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

Make sure your Microsoft 365 admin has assigned licenses and roles to people in your organization. For more information about this process, refer to [Assign licenses](assign-licenses.md) and [Assign roles](assign-user-roles.md). To learn about Viva Insights licenses and other related requirements, refer to [Environment requirements](environment-requirements)

After the Microsoft 365 admin assigns licenses and roles—and after the app successfully processes organizational data from Azure Active Directory (AD)—you’ve fulfilled all setup requirements. 

>[!Important]
>Viva Insights won’t be ready for your organization to use immediately. After you finish assigning licenses, wait five days before using the app.

## Optional settings

To get the most out of the Viva Insights experience, you might want to set up a few optional controls. 

>[!Note]
>The **Insights Administrator** role is required to perform the following tasks.

### Customize privacy settings

#### Minimum group size

Set the minimum group size, which is the minimum aggregation threshold for insights. In other words, this is the smallest number of people that Viva Insights considers a “group.” Viva Insights shows insights about groups in the app in Teams and on the web, on the **Organization trends** page. You’ll need to make this number at least 10.

#### End-user opt-out

Select **End-user opt-out** to grant users the option to opt out of having their user metrics made available in advanced insights line-level query results from the person query. When users opt out, future person queries and those that refresh each week are affected. Opt-out doesn’t apply to aggregated insights (like those on the Organization trends page) and query results from collaboration events (like meetings). 

Users can find opt-out settings in their Viva Insights app in Teams or on the web under Settings > Privacy. After you turn on the **End-user opt-out** control, users who already opted out of Viva Insights through their app in Teams or on the web are automatically opted out of person query data. Settings take effect after one day. Users can opt back in to Viva Insights whenever they want and they’ll see their previously saved settings. 

#### Save changes

After you’re done making changes to group size and/or opt-out settings, select **Save changes**.

## Customize manager settings 

Use the **Manager settings** page to allow managers to see aggregated collaboration insights. These insights appear in the Viva Insights app in Teams or on the web, under **Organization trends**. Learn more about manager settings in [Manager settings](manager-settings.md). 

### Prepare and upload organizational data 

By default, Viva Insights uses your organization’s Azure AD data. This data automatically feeds into Viva Insights, so you don’t need to do anything extra to set up organizational data in the advanced insights app. If you want to upload your organizational data as a .csv file instead of using Azure AD, follow the guidance in [Prepare organizational data](../admin/prepare-org-data.md) and [Upload organizational data (first upload)](../admin/upload-org-data-first.md). After you upload a file, here’s the basic process:

1. Data mapping – You map the uploaded data to the applicable field names. For details, refer to Field mapping.
1. Data validation – Viva Insights validates the data. When validation completes successfully, you'll see a confirmation message. If validation wasn’t successful, you’re  advised what to do next. For details, refer to Validation.
1. Data processing – Viva Insights processes the validated data. When the processing is done, you'll see a message that setup is complete.

## Related topics

[Manager settings](manager-settings.md)

[Prepare organizational data](../admin/prepare-org-data.md)

[Upload organizational data (first upload)](../admin/upload-org-data-first.md)