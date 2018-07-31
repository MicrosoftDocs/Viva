---
# Metadata Sample
# required metadata

title: Workplace Analytics privacy and data access
description: Discusses the privacy and data access controls available in Workplace Analytics.  
author: madehmer
ms.author: rodonahu
ms.date: 07/19/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Workplace Analytics privacy and data access

## Introduction

Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

>[!Important]
>Please consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

This document introduces the privacy controls available to Workplace Analytics administrators. You control both the data and access to the data in Workplace Analytics.

### Video: Privacy

Watch this video to learn how Workplace Analytics handles employee data privacy, and how the Workplace Analytics admin can configure their privacy settings.

[<img src="../Images/WpA/setup/Privacy.png" alt="Privacy video">](https://aka.ms/WpAPrivacy_Video)

### You decide who gets to see what data

Organizations decide who can have access to seeing the data in Workplace Analytics. You should ensure that primary users receive suitable training in privacy, your company’s policies, and other applicable subject areas before being granted access to the data. The following levels of permission provide access to the data:

* **Analyst (Limited)** gives access to the Workplace Analytics Home Page and Explore Metrics features where minimum group size is enforced.
* **Analyst** gives full access to all product features except the administrator features.
* **Administrator role** gives access to administrator features only.
* **Program manager** gives access to the Workplace Analytics Home page and lets program managers explore metrics in cases where the minimum group size is enforced. PMs also have access to the Solutions tab and its Manage page, on which they can set up programs, and to its Track page, on which they can track the progress of active or ended programs.

## You control the data that Workplace Analytics uses

You retain full control over what data is used and how it is used within Workplace Analytics. Workplace Analytics uses Office 365 email and calendar metadata and external data defined by your organization to compute how much time groups within your organization spend on email and in meetings, and with whom.

## Data from Office 365

Office 365 email and calendar metadata provides the foundation for all Workplace Analytics analysis, so the first step is to determine which users you want to include. When you choose a user to be included, Workplace Analytics uses the following information from that user’s mailbox and calendar.

### Header information from emails

* Who the sender is.
* Who the recipient is.
* When was the email sent.
* What the subject line is.

### Header information from meetings

* Who organized the meeting.
* Who the invitees are and what their attendee status is.
* When the meeting was scheduled for.
* Where the meeting was scheduled to be held.
* What the subject line is.

>[!Important]
>Attachments and text in the body of emails and meetings are never used by Workplace Analytics. Furthermore, rights-managed and private emails and meetings are excluded altogether.

## Organizational data

Workplace Analytics combines Office 365 email and calendar metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions. Organizational data is contextual information about your employees (for example: job title, level, location) and can come from human resources, information systems, or other line of business data stores. For more information, see [Prepare organizational data](~/setup/prepare-organizational-data.md).

The organizational data set is combined with the Office 365 email and calendar metadata to produce the complete data set that is analyzed for insights. The data sets are combined using the email addresses of the users, but the email addresses are never shown in Workplace Analytics through dashboards or query results.

Please note that other information provided in the organizational data set is exposed in Workplace Analytics dashboards and reports. Care must be taken to ensure the data set does not include personal data (such as employee ID).

## Privacy settings

Workplace Analytics has three types of administrator controls, User Inclusion, User Data Exclusion, and Level of Detail Displayed to enable you to define specific criteria that will exclude meetings and emails from analysis.

### User inclusion

You decide which users to include by only assigning Workplace Analytics licenses to those people.

### User data exclusion

For the users that you choose to include, you can decide to exclude data based upon the following:

* **Keywords in subject line** excludes email and meetings that contain in their subject lines specific keywords that you define.
* **Email address and domain** excludes email and meetings to or from specific users, or all users from the specified domain.

>[!Note]
>Exclusion occurs before metadata is processed within Workplace Analytics. These exclusions will affect the data by counting any meetings or email with these domains as if they never happened. Consider excluding only the most sensitive domains.

### Level of detail displayed

* **Subject lines displayed** - In meeting query results, you can control whether subject lines are included or not. By default, subject lines are not shown in query results. Subject lines are useful for analysts that want to set up meeting exclusion rules or query meeting data.

* **Minimum aggregation size** - In Explore metrics, you can set the minimum group size required to display data. By default, the minimum group size is set to five.

## Data retention policy

### For active tenants

<!-- Note as of 25 JUNE 2018: We're discussing this wording today. -->

>[!Note]
>An active tenant is a tenant that has one or more valid Workplace Analytics licenses.

By default, Workplace Analytics maintains tenant data for only the preceding 24 months, which is a rolling window of 24 months of data. This means that Workplace Analytics will not have any tenant data that is older than 24 months.

<!-- REMOVED PER NIRAJ 25 JUNE 2018
Even though the default value is 24 months, the rolling windows are configurable at the tenant level. As a tenant, you can lengthen your data-retention period for analysis purposes, or shorten your data-retention period for other purposes, such as GDPR requirements or company policy.  -->

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

<!-- REMOVED PER NIRAJ 25 JUNE 2018
>[!Note] 
>The number of days is configurable for different inactive tenant states. Example: A customer uploaded sensitive data by mistake and wants to be explicitly deprovisioned quickly instead of waiting for 210 days [expired state (30 days) + disabled state (90 days) + deprovisioned state (90 days)].
-->