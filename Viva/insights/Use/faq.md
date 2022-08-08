---

title: Advanced insights FAQ
description: Frequently asked questions about advanced insights for the advanced insights app with Microsoft Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: reference
ms.localizationpriority: medium
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Advanced insights FAQ

The most commonly asked questions and answers about the analysis tools for Microsoft Viva Insights in the advanced insights app are grouped into the following sections:

* [Functionality and features](#functionality-and-features)

  * [Roles](#roles)
  * [Privacy and compliance](#privacy-and-compliance)
  * [Language support](#language-support)

* [Setup and configuration](#setup-and-configuration)
* [Organizational data](#organizational-data)

* [Use advanced insights](#use-advanced-insights)

  * [Meeting exclusions](#meeting-exclusions)
  * [Data validation, verification, and use](#data-validation-verification-and-use)
  * [Explore the stats](#explore-the-stats)
  * [Query designer](#query-designer)

## Functionality and features

### Roles

##### Q1. Is Viva Insights a tool for human-resource planning?

A1.  No. Viva Insights is a collaboration analysis tool for analyzing behavior and network patterns.

##### Q2. How do personal, manager, leader, and advanced insights differ?

A2. See [Introducing Microsoft Viva Insights](../introduction.md) for more information about the following different types of insights for the distinctly different audiences:

* Personal and private insights are for individual use only
* Manager insights are for people managers or team leads
* Leader insights are for business leaders
* Advanced insights are for analysts to run top-down analysis on advanced insights with aggregated and de-identified metrics

### Privacy and compliance

##### Q1. How much data does Viva Insights collect?

A1.  Initially 13 months' worth of data is collected and processed for Viva Insights. Through weekly refreshes, the system continues to increase this history until 27 months’ worth of data is collected. As a Microsoft customer, you can file a request, such as for security reasons, to provide Viva Insights with less than this default amount; in that case, the minimum amount that can be collected is one month.

##### Q2. Does Viva Insights support a separate data environment that adheres to compliance and regulatory requirements such as those required by the government?

A2. Advanced insights aren't available in data cloud environments that Microsoft maintains for government agencies.

### Language support

##### Q1. Can I use the advanced insights app in a language other than English?

A1. Yes. See [Language support and guidelines](../overview/supported-languages.md).

##### Q2. Can I upload an organizational data file that has non-English words or letters?

A2. Yes. The organizational data file can have non-English words or letters. However, note the following:
  
* File names and individual rows can have non-English words or letters.
* Each column header must be mapped to an attribute with an English name.

##### Q3. Can I create a query with filters or meeting subject lines that contain non-English words or letters?

A3. Yes. You can use filters in queries that include the following:

* Attributes or values from your organizational data that include non-English words or characters.
* Meeting subject lines (which can include non-English words or characters) as specific filter criteria.

For more information, see [Customize a base metric in a query](/viva/insights/tutorials/customize-a-metric?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Setup and configuration

##### Q1. What's required to enable advanced insights?

A1. The main tasks required to enable advanced insights for your organization are:

* Assign licenses
* Assign roles
* Configure settings
* Upload organizational data

For details about setup, see [Set up Advanced insights](/viva/insights/setup/set-up-workplace-analytics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

##### Q2. What if my licensed population works in different time zones or has varying working hours?

A2. Not an issue. Viva Insights can determine each employee's time-zone value and their working hours, regardless of their location. For details, see [Default time zone](../use/system-defaults.md#default-time-zone).

##### Q3. Can I configure what data an analyst can access and use?

A3. You can assign the Analyst (Limited access) role to limit an analyst access to only [Explore the stats](explore-intro.md) data for advanced insights. See [Assign roles](/viva/insights/setup/assign-roles-to-wpa-admins?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and [User roles](/viva/insights/user-roles?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for more details.

##### Q4. Why are Start and End times so important during configuration?

A4. The **Start** and **End** time values determine the working hours for which data will be analyzed. They also determine the time period that is considered *after hours*. See [Working days and working hours](system-defaults.md#working-days-and-working-hours).

##### Q5. Is the number of analyst role assignments limited?

A5. No limit is imposed for Analyst roles.

##### Q6. In Data sources, who's included in the number of "Measured employees" on the Microsoft 365 data page?

A6. This number includes licensed employees who are also present in your organization's collaboration (Microsoft 365 or Office 365) data. For details, see [Origin of data counts](office-365-data.md#origin-of-data-counts).

##### Q7. Are people who are not assigned a license ignored?

A7. No, they aren't ignored but they aren't measured and their data isn't processed. However, as internal collaborators of measured employees, their collaboration data is used for analysis when measured employees collaborate with them through meetings, email, unscheduled calls, or instant messages. For details, see [Origin of data counts](office-365-data.md#origin-of-data-counts).

##### Q8. Do advanced insights in Viva Insights support user mailboxes in Sweden go-local?

A8. No, Advanced insights in Viva Insights does not currently support mailboxes in [Sweden go-local](/microsoft-365/enterprise/o365-data-locations#sweden). To get updated data for advanced insights, you can't have [licenses assigned](../setup/Assign-licenses-to-population.md) to users with mailboxes in Sweden go-local.
 
## Organizational data

##### Q1. What causes a failed or an invalid upload?

A1. An upload can fail if the data has invalid values, if it is missing required data, or if the validity threshold for reserved or optional data is set too high. This is common for custom fields in uploads after the organization's first upload. See the following for details:

* [Validation fails](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-fails) in _Upload organizational data (subsequent uploads)_
* [Validation fails](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-fails) in _Upload organizational data (first upload)_

##### Q2. For my first organizational data upload, should I add, edit, or replace?

A2.  For your first upload, you won't see any of these choices. For more details about your first upload, see [Upload organizational data](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). For more information about when to add or edit data in a subsequent upload, see [Subsequent uploads](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#file-upload).

##### Q3. For the [required fields](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#system-default-fields), what percentage is required for the validity threshold?

A3. PersonId and EffectiveDate fields must meet 100 percent of the validity threshold, because each row of data must have a PersonId for each person in your organization. The other required fields (such as ManagerID) must exceed 95 percent of the validity threshold. Note that the calculations for validity threshold consider only two kinds of data values: valid values and blank values. For a validity threshold set to 95 percent, the column will pass validation if fewer than five percent of the values in the column are blank and the rest are valid. However, if even one cell contains malformed data, the entire file upload will fail. See [Field column details](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-column-details) for more information.

##### Q4. What happens if an employee (who is represented by a PersonID) has more than one manager (represented by ManagerIDs)?

A4. Organizational data allows for the identification of only one single, primary manager. This manager is represented by the ManagerID for that PersonID on a given EffectiveDate. However, note that the Viva Insights admin can use the EffectiveDate field in the organizational data to indicate that an employee’s primary manager has changed from one month to the next.

##### Q5. Who gets the organizational data to upload?

A5. Usually, HR gives this data to the Viva Insights admin, who then [prepares](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and [uploads](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) it.

##### Q6. Who can access organizational data after it has been uploaded?

A6. For privacy reasons, no one can download the raw data that was uploaded. Viva Insights admins can view metadata about the organizational data on the [Data sources](data-sourcesv2.md) page, but they cannot see how the attribute values map to individual people.

## Use advanced insights

### Meeting exclusions

##### Q1. How are privacy settings and meeting-exclusion rules different?

A1. Admins set up the  _privacy settings_ for how data is extracted, such as preventing data from ever being included in any calculation. Note that changes to privacy settings apply to future data extractions and aren't retroactive to past data. See [Privacy settings](privacy-settings.md) and [Privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.

Analysts use _meeting-exclusion rules_ in queries to help ensure that the results accurately represent relevant meeting norms within the organization. Changes to these rules apply retroactively in the data. See [Meeting exclusion rules](/viva/insights/tutorials/meeting-exclusions-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.

##### Q2. Can meeting exclusion rule sets that I create be used by other analysts?

A2.  Yes. Anyone in your organization can use the meeting exclusion rules that anyone else in the organization has created. See [Application of meeting-exclusion rules](/viva/insights/tutorials/meeting-exclusion-concept?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#application-of-meeting-exclusion-rules) for details.

### Data validation, verification, and use

##### Q1. Why is my measured population less than the number of employees with assigned licenses?

A1. This can occur if you selected only a subset of the population for the analysis, or if your admin excluded a subset of the population from the organizational data that's uploaded. See [Assign licenses](/viva/insights/setup/assign-licenses-to-population?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), [Who to include in the data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#which-employees-to-include), and [Origin of data counts](office-365-data.md#origin-of-data-counts) for details.

##### Q2. Why do the totals seem too high for internal and external collaborators?

A2. The collaborator totals include the number of internal (or external) people with whom the measured employees have collaborated at least one time during the selected period. The totals that are included in the [Summary data](explore-metrics-external-collaboration.md#summary-data) on the **External collaboration** page don't change because of filters that have been applied in **Settings and filters**. For details, see [External collaboration](explore-metrics-external-collaboration.md).

##### Q3. Why doesn't the email or meeting trend line extend back for the entire historical 13-month period (or for the selected custom time period)?

A3. Business policies can affect the historical data that is processed for Viva INsights. As you view historical data, if you see a steady decline or point-in-time drop in email and/or meeting activity, it might be due to email having been archived. Another cause can be recurring meetings that are deleted before the data is extracted. However, this only impacts initial baseline data, because future deletions don't affect weekly data that was previously collected. On the **Sources** page, you can select a time period where the email and/or meeting activity is stable. For details, see [Microsoft 365 data](office-365-data.md).

##### Q4. How does data for meetings and emails sent to distribution lists get processed?

A4. Email and meetings data for a distribution list is processed as a single entity or person. It does not expand the distribution list and assign meeting and email hours to its members. For more accurate data, upload the organizational data attributes for these lists by adding attributes of the distribution-list members or whatever best describes the list population. See [Subsequent uploads](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.

##### Q5. What collaboration information is processed from Microsoft Teams?

A5. Teams provides information about collaboration activities, namely direct messages (chats) and calls. It does not provide information about Teams channels.

##### Q6. When a person sends a message or meeting invite for a group’s shared mailbox or on behalf of another person, who gets credit for sending it?

A6. It depends on the type of mailbox and which permissions are set for the Exchange Online mailbox. For details, see [Mailbox permissions](/Exchange/recipients/mailbox-permissions).  

* A **shared mailbox** (Microsoft 365 group mailbox) typically has a number of group members that share access and permissions for the group mailbox. An example of a shared mailbox is `LeadershipTeam@Contoso.com`. For details, see [Which permissions you should use in shared mailboxes](/exchange/collaboration-exo/shared-mailboxes#which-permissions-should-you-use).

  * **Send As** permission - When a group member with Send As permission for a shared mailbox sends a message or meeting invitation from the group mailbox, Exchange gives credit to the shared mailbox instead of any single person in the group. Viva Insights does not use this action in its calculations.
  * **Send on Behalf** permission – This permission isn't available for shared mailboxes in Exchange Admin Center. However, if it is set with PowerShell (GrantSendonBehalf parameter), the person who sends the message gets credit for it in Viva Insights calculations.

* An **individual mailbox** (or a linked mailbox) with a primary mailbox owner can link or give delegate access and one of the following permissions to another person to send messages or meeting invites for the primary mailbox owner. For example, an assistant with delegate access can send a message or meeting invite from their manager's mailbox. A delegate can have one of the following permissions. For details, see [Give mailbox permissions to another user](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user).

  * **Send As** permission – The primary owner of the mailbox gets credit for sending the message or invite in Viva Insights calculations.
  * **Send on Behalf** permission - The person who sends the message on behalf of the mailbox owner gets the credit in Viva Insights calculations.
  * Both **Send As** and **Send on Behalf** permissions – If the delegate person has both permissions set, the **Send As** permissions are used and that person does not get credit for sending the message or invite in Exchange and therefore Viva Insights credits the owner of the mailbox in calculations.

##### Q7. Why don't I see data from this week in my analyses?

A7. Microsoft 365 collaboration data is updated weekly for advanced insights and other applicable analysis. Each Monday, Viva Insights processes your organization's collaboration data from the preceding week, which includes the previous Sunday through Saturday. For example, on Monday, November 15th, analysis will include data through the previous Saturday, November 13th.

##### Q8. Why don't I see last week's data in my analyses?

A8. I expect my analysis to include last week's collaboration data and I only see data through the previous Sunday. All multi-day periods (weeks and months) that are included in analysis reflect the first day of the specified time period. For example, for a query aggregated by week, you’ll see it starts with Sunday. If you see a "November 7th” row in a weekly aggregated query, it means that the metrics include data through Saturday, November 13th.

### Explore the stats

##### Q1. Why do I have fewer "filtered employees" than "measured employees" with no filters applied?

A1. Employee data can change based on the Settings and filters that are selected for **Explore the stats** or **Solutions** data. These settings aren't necessarily considered filters but can still cause totals to vary. For details, see [Settings and filters in Explore the stats](explore-page-settings.md).

##### Q2. How does Viva Insights estimate the cost of low-quality meetings? Can I customize this estimate?

A2. Admins can include optional hourly-rate data in the organizational data upload, which they can then use to calculate the total cost of low-quality meetings for the [Meetings overview](explore-metrics-meetings-overview.md). If this organizational data is provided, cost is calculated as the person's default hourly rate for the organization multiplied by the number of low-quality meeting hours. If no hourly rate is assigned to a meeting participant, a default hourly rate of $75 is used. On the **Settings** page, admins can change the value in the Hourly Rate field from its default value to another hourly rate.

##### Q3. Why are a group's total meeting hours (included as part of working hours and after-hours work) larger than the group's total meeting hours for the week?

A3. This can occur because of the way Viva Insights calculates meeting hours. The meeting-hours total includes adjusted hours for attended meetings, while total working hours and after-hours work include the number of meeting hours (not adjusted) for scheduled meetings.

This discrepancy can occur when meetings overlap. Viva Insights doesn't know which meetings were attended, so the meeting hours total will include adjusted hours, which are an estimate of time actually spent in meetings. For example, let's say a group of five employees is double booked for two meetings from 4:30 to 5:30 PM, and the group's workday ends at 5:00 PM. For this scenario, Viva Insights adjusts the meeting hours to one hour, since the group can't attend two meetings at the same time. However, Viva Insights doesn't adjust for the two scheduled meetings, which results in it adding five hours to total working hours and five hours to after-hours work. The group can avoid this discrepancy by declining any scheduled meetings that they don't attend.

##### Q4. What is the total workday length assumed for calculating focus hours?

A4. If measured employees or internal collaborators have their time zones defined as part of your organizational data, Viva Insights uses their individual time-zone settings for working hours, focus hours, and other time-related metrics. However, if the organizational data does not define a time zone for an employee, Viva Insights uses the default time-zone setting that your admin sets in Viva Insights for that employee. For more details, see [Time zone setting](system-defaults.md) and [Focus hours and fragmented hours](explore-metrics-week-life.md#focus-hours-and-fragmented-hours).

### Query designer

##### Q1. For a group-to-group query, what's the difference between the results for "Collaborators Within Group" and for "Same group as Time Investor?"

A1.  If the result of a query defines the same set of people as members of both the time investors and collaborators groups, and these individuals also match any defined filters, then the collaborators are grouped together under the **Collaborators Within Group** results. The **Same group as Time Investor** results apply when a time-investor group allocates time only to themselves if no other groups are participating in the meeting or email. See [Group-to-group query output](csv-query-output-file.md#group-to-group-query-output) and [Overview of time allocation](/viva/insights/tutorials/group-to-group-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#overview-of-time-allocation) for more details.

##### Q2. How do I analyze collaboration hours at my company for a specific time frame, such as 8 PM to 8 AM?

A2. You can use the Collaboration hours metric to filter for a specific time frame, regardless of when it occurs. Note that query results that use the Collaboration hours to filter for a time period that includes after-hours time, such as 8 PM to 8 AM, will include all people who collaborated during this time regardless of if they have this time period set as their working or non-working hours on their calendar.

##### Q3. Why don't totals for meeting hours and email hours match up with totals for working hours and after hours in person query output?

A3. Because totals for working hours and after hours calculate the "time booked on your calendar" instead of "time in meetings." Calculations for total meeting hours (time in meetings) adjusts the duration time to account for double-booked meetings, where a person has two meetings scheduled at the same time or times that overlap on the calendar. A heuristic logic orders which meetings a person likely attended and assigns time accordingly. For more details, see [Person query output](../use/csv-query-output-file.md#person-query-output).

##### Q4. When I download and view a query, why is the data unreadable or not shown correctly in Excel?

A4. You probably opened the .csv file as is. For Excel to show the data correctly, you need to import the .csv file into Excel. If you're using Excel 2016, follow the steps in [Download and import query results](view-download-and-export-query-results.md#download-and-import-query-results). For other versions of Excel, open **Help** in Excel and then search for the instructions on how to import a .csv file.

##### Q5. Why don’t a person’s low-quality meeting hours equal the sum of their redundant, conflicting, and multitasking meeting hours in my query?

You might expect the total number of redundant, conflicting, and multitasking meeting hours to equal the total number of low-quality meeting hours. However, sometimes they won’t equal because of how conflicting meeting hours are calculated. For more details, see [Low-quality meeting hours](../use/explore-metrics-meetings-overview.md#low-quality-meeting-hours), [Conflicting meeting hours](../use/explore-metrics-meetings-overview.md#conflicting-meeting-hours), and [Calculation variables](../use/explore-metrics-meetings-overview.md#calculation-variables).
