---
# Metadata Sample
# required metadata

title: Workplace Analytics privacy and data access
description: Discusses the privacy and data access controls available in Workplace Analytics  
author: madehmer
ms.author: v-midehm
ms.date: 2/21/2019
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Workplace Analytics privacy and data access

## Introduction

Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

>[!Important]
> Consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

This document introduces the privacy controls available to Workplace Analytics administrators. You control both the data and access to the data in Workplace Analytics.

### You decide who gets to see what data

Organizations decide who can have access to see the data in Workplace Analytics. You should ensure that primary users receive suitable training in privacy, and in your company’s policies and other applicable subject areas, before being granted access to the data. The following levels of permission provide access to the data:

* **Analyst (Limited Access)** gives access to the Workplace Analytics Home Page and Explore Metrics features where minimum group size is enforced.
* **Analyst** gives full access to all product features except the administrator features.
* **Administrator role** gives access to administrator features only (Settings and Data Source pages).
* **Program manager** gives access to the Workplace Analytics Home page and lets program managers explore metrics in cases where the minimum group size is enforced. PMs also have access to the Solutions tab and its Manage page, on which they can set up programs, and to its Track page, on which they can track the progress of active or ended programs.

### You control the data that Workplace Analytics uses

You retain full control over what data is used and how it is used within Workplace Analytics. Workplace Analytics uses Office 365 email and calendar metadata and external data defined by your organization to compute how much time groups within your organization spend on email and in meetings, and with whom.

## Data from Office 365

Office 365 email and calendar metadata provides the foundation for all Workplace Analytics analysis, so the first step is to determine which users you want to include. When you choose a user to be included, Workplace Analytics uses the following information from that user’s mailbox and calendar:

### Header information from emails

* Who the sender is
* Who the recipient is
* When was the email sent
* What the subject line is

### Header information from meetings

* Who organized the meeting
* Who the invitees are and what their attendee status is
* When the meeting was scheduled
* Where the meeting was scheduled to be held
* What the subject line is

>[!Important]
>Attachments and text in the body of emails and meetings are never used by Workplace Analytics. Furthermore, rights-managed and private emails and meetings are excluded altogether.

## Organizational data

Organizational data is contextual information about your employees (for example: job title, level, location) and can come from human resources, information systems, or other line-of-business data stores. Workplace Analytics combines Office 365 email and calendar metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

The organizational data set is combined with the Office 365 email and calendar metadata to produce the complete data set that is analyzed for insights. The data sets are combined using the email addresses of the users, but the email addresses are never shown in Workplace Analytics through dashboards or query results.

Note that other information provided in the organizational data set is exposed in Workplace Analytics dashboards and reports. Take care to ensure that the data set does not include personal data (such as the employee ID).
For more information about organizational data, see [Prepare organizational data](~/setup/prepare-organizational-data.md).

<!-- 8/24 ADDING NEW SECTION ON DATA RETENTION POLICY. This is temporary until the new policy is announced. -->

## Data access after license expiration

If your Workplace Analytics licenses expire, you have a 90-day period to download data, in the form of query results. After this 90-day period has passed, you will no longer have access to the Workplace Analytics site. 

**To download query results**

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, If prompted, sign in with your work account.
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

## Related topic

[Workplace Analytics privacy settings](../use/settings.md#privacy-settings)