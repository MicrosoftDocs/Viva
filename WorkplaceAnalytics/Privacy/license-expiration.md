---
# Metadata Sample
# required metadata

title: Data access after license expiration
description: Accessing your organization's data after expiration of your Workplace Analytics license
author: paul9955
ms.author: v-pascha
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

<!-- 8/24 ADDING NEW SECTION ON DATA RETENTION POLICY. This is temporary until the new policy is announced. -->

# Data access after license expiration

If your Workplace Analytics licenses expire, you have until the end of your grace period to download data, in the form of query results. After this period has passed, you will no longer have access to the Workplace Analytics site. (The duration of the grace period varies between countries and plans; typically it is either 30 days for direct purchases or 90 days for volume-licensing purchases.) 

**To download query results**

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, sign in with your work account.
2. In the left navigation, expand **Analyze** and then select the **Queries** page.
3. Select **Results**. The Results page displays previously run queries.
4. In the row of a particular query, select **Download**. The query results are downloaded in a .csv file which is archived into a .zip file.

<!-- 
8/23 REMOVING ENTIRE OLD DATA RETENTION POLICY SECTION FOR NOW. TILL NEW TEMPORARY WORDING IS READY.

FIRST SECTION TO REMOVE: 

## Data retention policy

### For active tenants

>[!Note]
>An active tenant is a tenant that has one or more valid Workplace Analytics licenses.

By default, Workplace Analytics maintains tenant data for only the preceding 24 months, which is a rolling window of 24 months of data. This means that Workplace Analytics will not have any tenant data that is older than 24 months.

END OF FIRST SECTION REMOVED 8/23 -->

<!-- REMOVED PER NIRAJ 25 JUNE 2018
Even though the default value is 24 months, the rolling windows are configurable at the tenant level. As a tenant, you can lengthen your data-retention period for analysis purposes, or shorten your data-retention period for other purposes, such as GDPR requirements or company policy.  -->

<!-- 8/23 REMOVE FOR NOW SECOND SECTION:

### For inactive tenants

>[!Note]
>An inactive tenant is a tenant that has no active Workplace Analytics user licenses.

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

