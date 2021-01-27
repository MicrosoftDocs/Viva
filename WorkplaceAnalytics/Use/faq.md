---

title: Workplace Analytics FAQ
description: Frequently asked questions about Workplace Analytics
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal
ms.prod: wpa
---

# Frequently Asked Questions for Workplace Analytics

The most commonly asked questions and answers about Workplace Analytics are grouped into the following sections:

[Product information](#product-information)

* [Product roles](#product-roles)
* [Privacy and compliance](#privacy-and-compliance)
* [Language support](#language-support)

[Workplace Analytics setup](#workplace-analytics-setup)

* [Setup and configuration](#setup-and-configuration)
* [Organizational data](#organizational-data)

[Use Workplace Analytics](#use-workplace-analytics)

* [Meeting exclusions](#meeting-exclusions)
* [Data validation, verification, and use](#data-validation-verification-and-use)
* [Explore the stats](#explore-the-stats)
* [Queries](#queries)

## Product information

### Product roles

##### Q1. Is Workplace Analytics considered a tool for human-resource planning?

A1.  No. Workplace Analytics is a collaboration analysis tool that can be used to analyze behavior and network patterns.

##### Q2. How do MyAnalytics and Workplace Analytics differ?

A2. MyAnalytics presents personal and private insights to Microsoft 365 users in Outlook through [digest emails](../myanalytics/use/email-digest-2.md), [inline suggestions](../myanalytics/use/mya-notifications.md) and the [Insights Outlook add-in](../myanalytics/use/add-in.md). It can also be accessed through a web [dashboard](../myanalytics/use/dashboard-2.md).

Workplace Analytics is a tool that is used by organizations for running top-down analysis and it computes only aggregated and anonymized metrics.

### Privacy and compliance

##### Q1. How much data does Workplace Analytics collect?

A1.  Workplace Analytics initially collects and processes 13 months' worth of data. Through weekly refreshes, Workplace Analytics continues to increase this history until 27 months’ worth of data is collected. Customers can file a request, for security reasons, to provide Workplace Analytics with less than this default amount; in that case, the minimum amount that can be collected is one month.

<!-- REMOVING THIS SCARY QUESTION FOR NOW

##### Q6. Can the data gathered for Workplace Analytics be accessed by Microsoft or by anybody in the tenant or company?

A6.  No. All data is encrypted and kept available only for queries and for Explore the stats data.
-->

##### Q2. Does Workplace Analytics support a separate data environment that adheres to compliance and regulatory requirements such as those required by the government?

A2. Workplace Analytics is not available in data cloud environments that Microsoft maintains for government agencies.

### Language support

##### Q1. Can I upload an organizational data file that has non-English words or letters?

A1. Yes. The organizational data file can have non-English words or letters. Note the following: 
   
 * File names and individual rows can have non-English words or letters.
 * Each column header must be mapped to an attribute with an English name.

##### Q2. Can I construct a query with filters and/or meeting subject lines that contain non-English words or letters?

A2. Yes. You can use filters in queries that include the following:

 * Attributes or values from your organizational data that include non-English words or characters.
 * Meeting subject lines (which can include non-English words or characters) as specific filter criteria.

For more information, see [Customize a base metric in a query](../tutorials/customize-a-metric.md).

## Workplace Analytics setup

### Setup and configuration

##### Q1. What are the basic steps to enable Workplace Analytics?

A1. The main tasks required to enable Workplace Analytics for your organization are:

* Assign licenses
* Assign roles
* Configure settings
* Upload organizational data

For complete information about setup, see [Set up Workplace Analytics](../setup/set-up-workplace-analytics.md).


<!--  KEEP THIS OUT FOR NOW. POINT TO THE JEREMY/GAURAV/DANNY TOPIC AS SOON AS WE PUBLISH IT.

##### Q2. Which Office 365 licenses are required for Workplace Analytics users?

A2. The following license plans work: 
 * Exchange Online (EXO) Plan 1 (Office 365 Enterprise plan E1) 
 * Exchange Online (EXO) Plan 2 (Office 365 Enterprise plans E3, E4, or E5).

-->

##### Q2. Does it present a problem if my licensed population works in different time zones or has varying working hours?

A2. No. Workplace Analytics can determine each employee's time-zone value and their working hours, regardless of their location. To make this determination, Workplace Analytics carries out the steps that are described in [Default time zone](../use/system-defaults.md#default-time-zone).

##### Q3. Can I configure the user data that particular analysts can access and use?

A3. You can assign analysts the analyst (limited access) role, which limits them to view [Explore the stats](explore-intro.md) data. See [Assign Workplace Analytics roles](../setup/assign-roles-to-wpa-admins.md) and [User roles in Workplace Analytics](user-roles.md) for more details.

<!-- ^^^ *** After partitions ship, add them to this answer. *** ^^^ -->

##### Q4. Why are Start time and End time so important when configuring Workplace Analytics?

A4. The Start time and End time values determine the working hours for which data will be analyzed. They also determine the time period that is considered *after hours*. <!--(Note that the system time zone is checked once a week, so if an employee travels for a short time the change in their local time might not be captured and reflected in their Start and End times.) --> See [Working days and hours](system-defaults.md#working-days-and-hours).

##### Q5. Is there a maximum number of Workplace Analytics analyst roles that can be assigned?

A5. No. No limit is imposed by Workplace Analytics.

##### Q6. In the Workplace Analytics _Data sources_ section, on the "Office 365 data" page, you can see the number of "Measured employees." Is this the number of licensed users or the number of both licensed and un-licensed?

A6. Licensed. Specifically, this number refers to licensed employees who are also present in the collaboration (Office 365) data. For more information, see [Origin of data counts](office-365-data.md#origin-of-data-counts).

##### Q7. What happens with users who were not assigned a Workplace Analytics license? Are they ignored?

A7. No, they are not ignored but they are not measured and their data is not processed. However, as internal collaborators of measured employees, their collaboration data is used for analysis when measured employees collaborate with them through meetings, email, unscheduled calls, or instant messages. For details, see [Origin of data counts](office-365-data.md#origin-of-data-counts).

### Organizational data

##### Q1. What are common causes of a failure to upload an organizational data file into Workplace Analytics, or the invalidity of such a file?

A1. An upload can fail if the data has invalid values, if it is missing required data, or if the validity threshold for unrequired data is set too high; this is the case for custom fields in uploads after the organization's first upload. For more information, see the following:

* [Validation fails](../setup/upload-organizational-data.md#validation-fails) in _Upload organizational data (subsequent uploads)_
* [Validation fails](../setup/upload-organizational-data-1st.md#validation-fails) in _Upload organizational data (first upload)_

##### Q2. For my first organizational data upload, should I choose "append" or "replace"?

A2.  For your first upload, you will not have either of these choices. For more details about your first upload, see [Upload organizational data (first upload)](../setup/upload-organizational-data-1st.md). For more information about when to append or replace, see [Upload organizational data (subsequent uploads)](../setup/upload-organizational-data.md#file-upload).

##### Q3. For the [required fields](../setup/upload-organizational-data-1st.md#system-default-fields-table), what percentage does Workplace Analytics require for the validity threshold?

A3. Workplace Analytics requires that the PersonId and EffectiveDate fields meet 100% of the validity threshold, because each of row of data must have a PersonId for each person in your organization. The other required fields (such as ManagerID) must exceed 95% of the validity threshold. (Note that the calculations of validity threshold consider only two kinds of data values: valid values and blank values. This means that, for a validity threshold that's set to 95%, the column will pass validation if fewer than 5% of the values in the column are blank and the rest are valid. However, if even one cell contains malformed data, the entire file upload will fail.) For more information, see [Columns in the fields tables](../setup/upload-organizational-data.md#columns-in-the-fields-tables).

##### Q4. What happens if an employee (who is represented by a PersonID) has more than one manager (who would be represented by ManagerIDs)?

A4.  Organizational data allows for the identification of only one single, primary manager. This manager is represented by the ManagerID for that PersonID on a given EffectiveDate. However, note that the Workplace Analytics admin can use the EffectiveDate field in the organizational data to indicate that an employee’s primary manager has changed from one month to the next. 

##### Q5. Who obtains the organizational data that must be uploaded to Workplace Analytics?

A5. Usually, HR obtains this data and provides it to the Workplace Analytics admin who [prepares](../setup/prepare-organizational-data.md) and [uploads](../setup/upload-organizational-data-1st.md) it to Workplace Analytics.

##### Q6. Who can access organizational data after it has been uploaded to Workplace Analytics? 

A6. For privacy reasons, no one can download the raw data that was uploaded. Workplace Analytics admins can view metadata about the organizational data on the [Data sources](data-sourcesv2.md) page, but they cannot see how the attribute values map to individual people.

<!-- [NEAR FUTURE FOR THESE NEXT FIVE QUESTIONS, AFTER THE XLSX POSSIBILITY SHIPS]

##### Q3. What format do I save the data upload file as? 

A3.  Before you upload the data file, save it either as an .xlsx file or as a UTF-8 encoded .csv file. For more information, see [Format organizational data for upload](../setup/format-data-for-upload.md).

##### Q4. How should I name the organizational data file?   

A4.  The file name must contain only alphanumeric characters (letters and numbers), with no spaces or special characters. For example: **FileName2.xlsx** or **FileName2.csv**.

##### Q5. How do I format the header columns in the organizational data file? 

A5.  See [Structure an .xlsx file](../setup/format-data-for-upload.md#structure-an-xlsx-file) to formatting headers in .xlsx files and [Use only valid values and formats](../setup/format-data-for-upload.md#use-only-valid-values-and-formats-1) to format headers in .csv files. 

##### Q6. What format must the row field values have in the data file? 

A6.  To format rows in .xlsx files, see [Columns and rows](../setup/format-data-for-upload.md#columns-and-rows). To format rows in .csv files, see [Use only valid values and formats](../setup/format-data-for-upload.md#use-only-valid-values-and-formats-1).

##### Q7. Can the data contain double-byte characters? 

A7  Yes. The data can include double-byte characters, such as Japanese characters. If you are uploading a .csv file, it must first be saved as a UTF-8 encoded file. Otherwise, you can upload organizational data in an .xlsx file. To format rows in .csv files, see [Use only valid values and formats](../setup/format-data-for-upload.md#use-only-valid-values-and-formats-1).

-->

## Use Workplace Analytics

### Meeting exclusions

##### Q1. What is the difference between privacy settings and meeting-exclusion rules?

A1. Admins make  _privacy settings_ to change the way Workplace Analytics extracts data, such as preventing data from ever being included in any Workplace Analytics calculation. Note that privacy settings changes apply to future data extractions and are not retroactive to past data. For more information, see [Privacy settings](privacy-settings.md) and [Workplace Analytics privacy and data access](../privacy/privacy-and-data-access.md).

Analysts use _meeting-exclusion rules_ in Workplace Analytics queries to help ensure that query results accurately represent relevant meeting norms within the organization. Changes to these rules apply retroactively in the data. For more information, see [Meeting exclusion rules in Workplace Analytics](../tutorials/meeting-exclusions-intro.md).

##### Q2. Can other analysts use the meeting exclusion rule sets that I create?

A2.  Yes. Anyone in your organization can use the meeting exclusion rules that anyone else in the organization has created. For more information about meeting exclusion rules, see [Application of meeting-exclusion rules](../tutorials/meeting-exclusion-concept.md#application-of-meeting-exclusion-rules).

### Data validation, verification, and use

##### Q1. Why is my measured population less than the number of employees with assigned licenses?

A1.  This can happen if you selected only a subset of your population for data analysis, or if your admin excluded a subset of the population from the organizational data that's uploaded into Workplace Analytics. For more details, see [Assign licenses](../setup/assign-licenses-to-population.md) and [Who to include in the data](../setup/prepare-organizational-data.md#which-employees-to-include) in [Prepare organizational data](../setup/prepare-organizational-data.md), and see [Origin of data counts](office-365-data.md#origin-of-data-counts).

##### Q2. Why do the totals seem too high for internal and external collaborators?

A2. The collaborator totals include the number of internal (or external) people with whom the measured employees have collaborated at least one time during the selected period. The totals that are included in the [Summary header](explore-metrics-external-collaboration.md#summary-header) on the **External collaboration** page do not change because of filters that have been applied in **Page settings**. For details, see [External collaboration](explore-metrics-external-collaboration.md).

##### Q3. Why doesn't the email or meeting trend line extend back for the entire historical 13-month period (or for the custom time period that I set)?

A3. Business policies can affect the historical data that is processed by Workplace Analytics. As you view historical data, if you see a steady decline or point-in-time drop in email and/or meeting activity, it might be due to email having been archived. Another cause can be recurring meetings that are deleted before the data is extracted. However, this only impacts initial baseline data, because future deletions do not affect weekly data that was previously collected. On the **Sources** page, you can select a time period where the email and/or meeting activity is stable. For more information, see [Office 365 data summary](office-365-data.md).

##### Q4. How does Workplace Analytics process data for meetings and emails sent to distribution lists?

A4. Workplace Analytics processes email and meetings data for a distribution list as a single entity or person. It does not expand the distribution list and assign meeting and email hours to its members. For more accurate data, upload the organizational data attributes for these lists by adding attributes of the distribution-list members or whatever best describes the list population. See [Upload organizational data](../setup/upload-organizational-data.md) for detailed steps.

##### Q5. What collaboration information is processed from Microsoft Teams?

A5. Teams provides information about collaboration activities, namely direct messages (chats) and calls. It does not provide information about Teams channels.

##### Q6. When a person sends a message or meeting invite for a group’s shared mailbox or on behalf of another person, who gets credit for sending it?

A6. It depends on the type of mailbox and which permissions are set for the Exchange Online mailbox. For details, see [Mailbox permissions](https://docs.microsoft.com/Exchange/recipients/mailbox-permissions).  

* A **shared mailbox** (Microsoft 365 group mailbox) typically has a number of group members that share access and permissions for the group mailbox. An example of a shared mailbox is `LeadershipTeam@Contoso.com`. For details, see [Which permissions you should use in shared mailboxes](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes#which-permissions-should-you-use).

  * **Send As** permission - When a group member with Send As permission for a shared mailbox sends a message or meeting invitation from the group mailbox, Exchange gives credit to the shared mailbox instead of any single person in the group. Workplace Analytics does not use this action in its calculations.
  * **Send on Behalf** permission – This permission is not available for shared mailboxes in Exchange Admin Center. However, if it is set with PowerShell (GrantSendonBehalf parameter), the person who sends the message gets credit for it in Workplace Analytics calculations.

* An **individual mailbox** (or a linked mailbox) with a primary mailbox owner can link or give delegate access and one of the following permissions to another person to send messages or meeting invites for the primary mailbox owner. For example, an assistant with delegate access can send a message or meeting invite from their manager's mailbox. A delegate can have one of the following permissions. For details, see [Give mailbox permissions to another user](https://docs.microsoft.com/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user).

  * **Send As** permission – The primary owner of the mailbox gets credit for sending the message or invite in Workplace Analytics calculations.
  * **Send on Behalf** permission - The person who sends the message on behalf of the mailbox owner gets the credit in Workplace Analytics calculations.
  * Both **Send As** and **Send on Behalf** permissions – If the delegate person has both permissions set, the **Send As** permissions are used and that person does not get credit for sending the message or invite in Exchange and therefore Workplace Analytics credits the owner of the mailbox in calculations.

### Explore the stats

##### Q1. Why do I have fewer "filtered employees" than "measured employees" with no filters applied?

A1. Employee data can change based on the Page settings that are selected for **Explore the stats** or **Solutions** data. These settings are not necessarily considered filters but can still cause totals to vary. For details, see [Page settings](explore-metrics-external-collaboration.md#page-settings).

##### Q2. How does Workplace Analytics estimate the cost of low-quality meetings? Can I customize this estimate?

A2. Admins can include optional hourly-rate data in the organizational data upload, which they can then use to calculate the total cost of low-quality meetings for the [Meetings overview](explore-metrics-meetings-overview.md). If this organizational data is provided, cost is calculated as the person's default hourly rate for the organization multiplied by the number of low-quality meeting hours. If no hourly rate is assigned to a meeting participant, a default hourly rate of $75 is used. On the **Settings** page, admins can change the value in the Hourly Rate field from its default value to another hourly rate.

##### Q3. Why are a group's total meeting hours (included as part of working hours and after-hours work) larger than the group's total meeting hours for the week?

A3. This can occur because of the way Workplace Analytics calculates meeting hours. The meeting-hours total includes adjusted hours for attended meetings, while total working hours and after-hours work include the number of meeting hours (not adjusted) for scheduled meetings.

This discrepancy can occur when meetings overlap. Workplace Analytics doesn't know which meetings were attended, so the meeting hours total will include adjusted hours, which are an estimate of time actually spent in meetings. For example, let's say a group of five employees is double booked for two meetings from 4:30 to 5:30 PM, and the group's workday ends at 5:00 PM. For this scenario, Workplace Analytics adjusts the meeting hours to one hour, since the group cannot attend two meetings at the same time. However, Workplace Analytics doesn't adjust for the two scheduled meetings, which results in it adding five hours to total working hours and five hours to after-hours work. The group can avoid this discrepancy by declining any scheduled meetings that they do not attend.

##### Q4. What is the total workday length assumed for calculating focus hours?

A4. If measured employees or internal collaborators have their time zones defined as part of your organizational data, Workplace Analytics uses their individual time-zone settings for working hours, focus hours, and other time-related metrics. However, if the organizational data does not define a time zone for an employee, Workplace Analytics uses the default time-zone setting that your admin sets in Workplace Analytics for that employee. For more details, see [Time zone setting](system-defaults.md) and [Focus hours and fragmented hours](explore-metrics-week-in-the-life.md#focus-hours-and-fragmented-hours).


### Queries

##### Q1. For a group-to-group query, what's the difference between the results for "Collaborators Within Group" and for "Same group as Time Investor?"

A1.  If the result of a query defines the same set of people as members of both the time investors and collaborators groups, and these individuals also match any defined filters, then the collaborators are grouped together under the **Collaborators Within Group** results. The **Same group as Time Investor** results apply when a time-investor group allocates time only to themselves if no other groups are participating in the meeting or email. See [Group-to-group query output](csv-query-output-file.md#group-to-group-query-output) and [Overview of time allocation](../tutorials/group-to-group-queries.md#overview-of-time-allocation) for more details.

<!-- DOESN'T MATCH THE DESCRIPTION IN comparison-query.md, so REMOVING THIS QUESTION:  
##### Q3. What is the Manager effectiveness score?
A3. This score reflects how much time a person spends with their manager.
-->

##### Q2. How do I analyze collaboration hours at my company for a specific time frame, such as 8 PM to 8 AM?

A2. You can use the Collaboration hours metric to filter for a specific time frame, regardless of when it occurs. Note that query results that use the Collaboration hours to filter for a time period that includes after-hours time, such as 8 PM to 8 AM, will include all people who collaborated during this time regardless of if they have this time period set as their working or non-working hours on their calendar.

##### Q3. Why don't totals for meeting hours and email hours match up with totals for working hours and after hours in person query output?

A3. Because totals for working hours and after hours calculate the "time booked on your calendar" instead of "time in meetings." Calculations for total meeting hours (time in meetings) adjusts the duration time to account for double-booked meetings, where a person has two meetings scheduled at the same time or times that overlap on the calendar. A heuristic logic orders which meetings a person likely attended and assigns time accordingly. For more details, see [Person query output](../use/csv-query-output-file.md#person-query-output).

##### Q4. When I download and view a query, why is the data unreadable or not shown correctly in Excel?

A4. You probably opened the .csv file as is. For Excel to show the data correctly, you need to import the .csv file into Excel. If you are using Excel 2016, follow the steps in [Download and import query results](view-download-and-export-query-results.md#download-and-import-query-results). For other versions of Excel, open **Help** in Excel and then search for the instructions on how to import a .csv file.

##### Q5. Why don’t a person’s low-quality meeting hours equal the sum of their redundant, conflicting, and multitasking meeting hours in my query?

You might expect the total number of redundant, conflicting, and multitasking meeting hours to equal the total number of low-quality meeting hours. However, sometimes they won’t equal because of how conflicting meeting hours are calculated. For more details, see [Low-quality meeting hours](../use/explore-metrics-meetings-overview.md#low-quality-meeting-hours), [Conflicting meeting hours](../use/explore-metrics-meetings-overview.md#conflicting-meeting-hours), and [Calculation variables](../use/explore-metrics-meetings-overview.md#calculation-variables).

<!-- NEED MORE INFO BEFORE WE CAN INCLUDE THIS: 

##### Q6. When I download and view a query, why is the data unreadable or not shown correctly in Excel?

A6. You probably opened the .csv file as is. For Excel to show the data correctly, you need to *import* the .csv file into Excel. For Excel 2016 users, follow the steps in [Download and import a query](view-download-and-export-query-results.md#download-and-import-query-results). For other versions of Excel, open **Help** within Excel and search and use Excel's instructions on how to import a .csv file. 
-->


<!-- Deleting this. A WpA group is not really a thing. 

##### Q3. What is a Workplace Analytics group?

A3. A Workplace Analytics group is any group of people to be analyzed specific to Workplace Analytics, not to be confused with Office 365 groups or Security groups, these are configured via other steps in the office 365 tenant, Workplace Analytics group is how you refer to any group of individuals that are being analyzed (for example, individuals who have Workplace Analytics licenses).

<!-- DELETING BECAUSE JUST A LINK TO DOCS
##### Q5. What are low-quality meeting hours?

A5.  See the definition under [Person metrics](metric-definitions.md).
-->

<!-- MOVED TO REGULAR DOCS
##### Q1. When should I use a group-to-group query instead of a person-to-group query?

A1.  Use a [group-to-group query](../tutorials/group-to-group-queries.md) to understand how *one team* invested their collaboration time with other teams within and outside of the organization.

Use a [person-to-group query](../tutorials/person-to-group-queries.md) to understand how *individuals* invested their time with one or more collaborator teams within and outside of the organization. See [Queries overview](../tutorials/query-basics.md) for more details.

-->

<!-- THE FOLLOWING QUESTIONS WERE REMOVED AND PUT INTO THE REGULAR DOCS: 

##### Q3. How many people should be Workplace Analytics admins and/or analysts (and is there a maximum limit of these roles)?

A3.  This answer depends on the size of your organization and on your requirements for managing organizational data. The number of analysts should be as many as your organization requires to perform data analysis. See [Assign Workplace Analytics roles](../setup/assign-roles-to-wpa-admins.md) and [User roles in Workplace Analytics](user-roles.md) for more details. Workplace Analytics imposes no limit on the number of role assignments.   

##### Q4. Can our organization's Office 365 admin also be our Workplace Analytics admin?

A6. Yes. It's up to your organization to choose who gets assigned which role. See [Assign Workplace Analytics roles](../setup/assign-roles-to-wpa-admins.md) and [User roles in Workplace Analytics](user-roles.md) for more details.

##### Q7. Can I assign the Workplace Analytics admin and analyst roles to the same person?

A7.  Yes. It's up to your organization to choose who gets assigned which role. Best practice is to assign the admin and analyst roles to different people to prevent any misuse of or external linking to organizational data with collaboration metrics. See [Assign Workplace Analytics roles](../setup/assign-roles-to-wpa-admins.md) and [User roles in Workplace Analytics](user-roles.md) for more details .

##### Q8. Who should be assigned the role of analyst (limited access)?

A8. The analyst (limited access) role is for an analyst who needs access only to the insights shown in the Workplace Analytics *Explore the stats* data. See [User roles in Workplace Analytics](user-roles.md) and [Explore the stats](explore-intro.md) for more details.

##### Q9. After an admin changes configuration and privacy settings, when do the changes take effect in the data?  

A9. Different settings take effect at different times See the following table:

| Setting | Purpose | Effectiveness |
| ---- | ---- | ---- |
| Default time zone and working hours | Workplace Analytics uses these settings if personalized Outlook settings are not available in the user's mailbox. | These settings do not affect data that has already been processed. |
| Minimum group size | Suppress dashboard results for very small groups. | This setting takes effect immediately. |
| Hide meeting subject lines/Hash subject lines | Do not display subject line text in meeting query results. | This setting takes effect immediately, affecting data that has already been processed. |
| Processing exclusions | Any activity that involves these criteria will not be processed nor measured. | This setting will only exclude data that is processed after the exclusion has been added; it does not affect data that has already been processed. |

For more details, see [How often to upload](../setup/prepare-organizational-data.md#how-often-to-upload) in [Prepare organizational data](../setup/prepare-organizational-data.md).

##### Q14. Can I assign multiple Workplace Analytics roles to one account?

A14. Yes. In the Azure Portal, you can assign multiple roles to one account but you can assign only one role at a time. In the Azure portal, add the first role, click **Select**, return to the user list, and then select the same account again to choose the next role for that account. (Note that role assignment in Workplace Analytics is performed in the Azure Portal and not in the Office 365 dashboard. See [Assign group-based licenses for Workplace Analytics](https://docs.microsoft.com/Workplace-Analytics/use/group-based-licensing).)

##### Q12. Making privacy settings affects what data?

A12. Privacy settings affect both Office 365 data (such as meeting subject lines) and org data (such as group size). After you make changes to privacy settings, those changes take effect after data is processed in the following month. Privacy-settings changes do not affect data that has already been extracted. (For example, the privacy settings for excluding email, meetings, and domains do not affect data retroactively.) For more information, see [Privacy settings](privacy-settings.md).

##### Q18. When can analysis start?

A18. Analysts can begin to conduct analyses after [privacy settings have been made](privacy-settings.md) and [organizational data has been uploaded](../setup/upload-organizational-data-1st.md). 

##### Q19. Can I exclude a single domain or a specific email address from being analyzed?

A19. Yes. You can specify domains or email addresses to exclude by using the Privacy settings in Workplace Analytics. See [Exclude domains or email addresses](privacy-settings.md#exclude-domains-or-email-addresses).

-->

<!-- MOVED TO THE REGULAR DOCS: 

##### Q2. In what format do I save the data-upload file? 

A2. Before you upload the data file, save it as a UTF-8 encoded .csv file in Excel. Follow the steps in [Save a workbook to text format (.txt or .csv)](https://support.office.com/en-us/article/Save-a-workbook-to-text-format-txt-or-csv-3E9A9D6C-70DA-4255-AA28-FCACF1F081E6) and select to save the file as a **CSV UTF-8** file:

![CSV UTF-8 file](../Images/WpA/Use/csv-utf-8.png)

##### Q3. How should I name the organizational data file?    

A3.  The file name must contain only alphanumeric characters (letters and numbers), with no spaces or special characters. For example: **FileName2.csv**.

##### Q4. Can the data contain double-byte characters? 

A4.  Yes. The data can include double-byte characters, such as Japanese characters. Note that the .csv file to be uploaded must be saved as a UTF-8 encoded file.

##### Q5. Can I append new columns onto an already existing organizational data file?

A5. Yes. You can append the existing organizational data to update attribute values for existing employees, to add new employees, or to add new attributes. Refer to Step 9 in the [File upload procedure](../setup/upload-organizational-data.md#file-upload) for details.

##### Q7. What are the meanings of the required fields in organizational data?

A7. These are the required fields: 

 * **PersonID.** This is the primary SMTP address of an employee, licensed or unlicensed. For example: ann@contoso.com

 * **ManagerID.** This is the primary SMTP address of the manager of the employee for which the data is being collected. For example: jered@contoso.com

 * **EffectiveDate.** The day, month, and four-digit year that represents the place in time at which the uploaded data for an individual is accurate.

 * **Organization.** The department the employee works for within the company. For example: *Marketing, IT, Sales, Operations*

 * **LevelDesignation.** The employee's level, which is represented as a string. This level is specific to your organization and can represent an employee's experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity.

For more information, see [Attribute reference](../setup/prepare-organizational-data.md#attribute-reference).

-->