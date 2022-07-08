---

title: Data retention policy
description: Accessing your organization's data after expiration of Microsoft Viva Insights subscriptions or removal of licenses
author: madehmer
ms.author: helayne
ms.topic: conceptual
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Data retention policy

How long does Microsoft Viva Insights in the advanced insights app and in Teams retain the data that's collected? The answer depends on the state of the Viva Insights user licenses:

* [Data retention for active tenants](#data-retention-for-active-tenants)
* [Data retention after a license is removed](#data-retention-after-a-license-is-removed)
* [Data retention and access after all subscriptions expire](#data-retention-and-access-after-all-subscriptions-expire)

## Data retention for active tenants

An active tenant is tenant that has one or more valid Viva Insights user licenses.

By default, Viva Insights initially collects, processes, and retains 13 months' worth of data. Then, through weekly refreshes, Viva Insights increases this history until 27 months' worth of data is collected. After this point, older collaboration data is deleted as newer collaboration data is collected.

This means that Viva Insights will not have any collaboration data that is older than 27 months.

Customers can file a request to initiate Viva Insights with less than 13 months of data. For this case, the minimum amount that can be collected is one month.

## Data retention after a license is removed

If the Viva Insights license is removed from a user, Viva Insights retains that user's collaboration data that was collected during the period the license was assigned. Admins can continue to query the collaboration activity that this user participated in before they left. The person's collaboration data will be deleted according to the overall retention policy that is described in [Data retention for active tenants](#data-retention-for-active-tenants).

To permanently remove data from users after licenses are removed, you can contact Microsoft customer support to request a collaboration data reset. (See [Get support](../overview/getting-support.md).)

For information about data deletion requests as handled under the GDPR, see [Support for handling data subject requests](data-protection-considerations.md#support-for-handling-data-subject-requests).

## Data retention and access after all subscriptions expire

If all of your subscriptions expire, you have until the end of your grace period to download data in the form of results. See [To download query results](#to-download-query-results) for details. The duration of the grace period varies between countries and plans. Typically, it is either 90 days for volume-licensing purchases or 30 days for other purchase types. All backend data will be deleted in accordance with the [Microsoft 365 Data Handling Standard](/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).

After this period has passed, you will no longer have access to Viva Insights in the Microsoft Teams app or in the cloud-based service.

#### To download query results

1. Open the cloud-based [advanced insights app](https://workplaceanalytics.office.com/)(if that link doesn't work, try [this link instead](https://workplaceanalytics-eu.office.com/)). If prompted, sign in with your work account.
2. Select **Analyze** > **Query designer** > **Results**.
3. In the row for the query results, select **Download** to download the results as a .csv file, which is archived as a .zip file.

## Related topic

[Get support](../overview/getting-support.md)
