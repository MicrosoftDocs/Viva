---
# Metadata Sample
# required metadata

title: Data retention policy
description: Accessing your organization's data after expiration of Workplace Analytics subscriptions or removal of licenses
author: paul9955
ms.author: v-pascha
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Data retention policy

How long does Workplace Analytics retain the data that it has collected? The answer depends on the state of the Workplace Analytics user licenses: 

 * [Data retention for active tenants](#data-retention-for-active-tenants)
 * [Data retention after a license is removed](#data-retention-after-a-license-is-removed)
 * [Data retention and access after all Workplace Analytics subscriptions expire](#data-retention-and-access-after-all-workplace-analytics-subscriptions-expire)

## Data retention for active tenants

An active tenant is tenant that has one or more valid Workplace Analytics user licenses.

By default, Workplace Analytics initially collects, processes, and retains 13 months' worth of data. Then, through weekly refreshes, Workplace Analytics increases this history until 27 months' worth of data is collected. 

By default, Workplace Analytics initially collects, processes, and retains 13 months' worth of data. Then, through weekly refreshes, Workplace Analytics increases this history until 27 months' worth of data is collected. After this point, older collaboration data is deleted as newer collaboration data is collected.

This means that Workplace Analytics will not have any collaboration data that is older than 27 months. 

Customers can file a request to initiate Workplace Analytics with less than 13 months of data; in that case, the minimum amount that can be collected is one month.

## Data retention after a license is removed

If the Workplace Analytics license is removed from a user, Workplace Analytics retains that user's collaboration data that was collected during the period the license was assigned. Admins can continue to query the collaboration activity that this user participated in before they left. The person's collaboration data will be deleted according to the overall retention policy that is described in [Data retention for active tenants](#data-retention-for-active-tenants). 

For information about data deletion requests as handled under the GDPR, see [Support for handling data subject requests](data-protection-considerations.md#workplace-analytics-support-for-handling-data-subject-requests).

## Data retention and access after all Workplace Analytics subscriptions expire

If all of your Workplace Analytics subscriptions expire, you have until the end of your grace period to download data in the form of query results; see [To download query results](#to-download-query-results). The duration of the grace period varies between countries and plans; typically it is either 90 days for volume-licensing purchases or 30 days for other purchase types. All backend data will be deleted in accordance with the [Office 365 Data Handling Standard](https://docs.microsoft.com/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).

After this period has passed, you will no longer have access to the Workplace Analytics site. 

#### To download query results

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, sign in with your work account.
2. In the left navigation, expand **Analyze** and then select the **Queries** page.
3. Select **Results**. The Results page displays previously run queries.
4. In the row of a particular query, select **Download**. The query results are downloaded in a .csv file which is archived into a .zip file.


<!-- 
8/23 REMOVING ENTIRE OLD DATA RETENTION POLICY SECTION FOR NOW. TILL NEW TEMPORARY WORDING IS READY.

END OF FIRST SECTION REMOVED 8/23 -->

<!-- REMOVED PER NIRAJ 25 JUNE 2018
Even though the default value is 24 months, the rolling windows are configurable at the tenant level. As a tenant, you can lengthen your data-retention period for analysis purposes, or shorten your data-retention period for other purposes, such as GDPR requirements or company policy.  -->

<!-- 8/23 REMOVE FOR NOW SECOND SECTION:

### For inactive tenants

#### User policy

Workplace Analytics will stop extracting user data within seven days after a user license is expired or removed. In other words, the next scheduled data extraction will not take place if it occurs at least seven days after the user license is revoked or expires.

#### Tenant lifecycle management

If no valid user license is currently allocated to the tenant, the policy depends on the tenant state:

* **Expired state** analysts can run queries for the next 30 days, as if the state were still active.
* **Disabled state** data will remain available for the next 90 days, but only in read-only mode. In this mode, no queries can be executed. Customers can download their data during this time.
* **Deprovisioned state** tenant data is not available to view or use. The data will be deleted within the next 90 days.

END OF SECOND SECTION REMOVED 8/23 -->

<!-- REMOVED PER NIRAJ 25 JUNE 2018
>[!Note] 
>The number of days is configurable for different inactive tenant states. Example: A customer uploaded sensitive data by mistake and wants to be explicitly deprovisioned quickly instead of waiting for 210 days [expired state (30 days) + disabled state (90 days) + deprovisioned state (90 days)].
-->
