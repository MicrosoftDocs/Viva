---
# Metadata Sample
# required metadata

title: Audit logs for Workplace Analytics  
description: Learn how to monitor Workplace Analytics activity with audit logs
author: madehmer
ms.author: madehmer
ms.date: 1/24/2019
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Workplace Analytics audit logs

The Office 365 audit logs are generated and accessed in the Office 365 portal. As an Exchange admin, you can access these logs to audit or track general user activities and actions, such as to see who accessed, or tried to access, or modified data. These logs include an audit section for Workplace Analytics activity, which typically includes sensitive data. You can monitor and track your organizational data for all user actions to ensure compliance with your organization's privacy and security policies.

## Requirements

To access the audit logs, you must meet the following requirements:

* To access the auditing section of the Office 365 Security & Compliance Center, you must have an Exchange Online license(included with Office 365 Enterprise E3 and E5 subscriptions).
* You must either be a global admin or have an Exchange admin role that provides access to the audit log. Exchange admin roles are controlled through the Exchange admin center. For more information, see Permissions in Exchange Online.

## Access the audit logs

* To access the audit log search page, visit [protection.office.com](https://protection.office.com), and then sign in to Office 365 using your work account. The audit logs are directly available through the Office 365 Security & Compliance Center.

> [!TIP]
> Use a private browsing session to access the Office 365 Security & Compliance Center, because using a regular session prevents the credentials with which you are currently logged on from being used. 
> * To open an InPrivate Browsing session in Internet Explorer or Microsoft Edge, press CTRL+SHIFT+P. 
> * To open a private browsing session in Google Chrome (called an incognito window), press CTRL+SHIFT+N.

## Search the audit logs

The Search area has an extensive list of activities that users can perform on files, folders, email, groups, permissions, directory services, Microsoft 365 applications, and much more. Admins can search the logs, for example, to see if a user has modified a file or folder, or changed any privacy settings, or deleted a document, or see who deleted it, and when. An admin can find out information such as how many queries a user ran, which query types, or how many reports the user downloaded or what data was downloaded. Administrative actions are also recorded, including actions carried out on e-discovery cases.

### To search for general user activities

1. Before you can search the Office 365 audit log, you (or another admin) must first turn on audit logging. To turn it on, just select Start recording user and admin activities on the Audit log search page in the Security & Compliance Center. (If you don't see this link, auditing has already been turned on for your organization.) After you turn it on, a message says that the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete. You only need to do this one time.
2. On the Home page of the Office 365 portal under the Security & Compliance section, in the left-hand navigation, expand Search & Investigation and then select Audit log search.
3. On the Audit log search page under Search, for Activities, select to Show results for all activities.
4. Select a listed activity to audit, which then shows a check mark next to it.

## Workplace Analytics activities

To narrow the search results for just Workplace Analytics activities:

1. On the Audit log search page, under Search, select Activities.
2. In the Search field, enter Microsoft Workplace Analytics activities and press Enter. For example, the following shows a list of Workplace Analytics Activities.

## View search results

On the Audit log search page, search results appear under Results. A maximum of 5,000 (newest) events are shown in increments of 150. To show more events, use the scroll bar in the Results pane or press Shift + End to show the next 150 events.

For detailed information and tips on searching, filtering, and exporting results in the audit log, see search the audit log.

The Results section includes the following information for each event returned by the search. To sort the results, select the column header you want to sort by.

## Search the audit logs by date

You can search the logs by date range using the Start date and End date fields. The last seven days are selected by default. The date and time are presented in Coordinated Universal Time (UTC) format. The maximum date range that you can specify is 90 days.

If the selected date range is greater than 90 days, an error appears. If you're using the maximum date range of 90 days, select the current time for Start date. Otherwise, you'll receive an error saying that the start date is earlier than the end date. If you've turned on auditing within the last 90 days, the date range can't start before the date that auditing was turned on.

## Search the audit logs by user

You can search audit log entries for activities performed by specific users. To do so:

1. Select the Users box and then enter one or more user names in it. The selected users appear inside the box. The user name looks like an email address; it's the account with which users log into Workplace Analytics. To return entries for all users (and service accounts), leave this box blank.

2. The audit log entries for the selected activities performed by the users you select in this box are shown in the results list. 


   The Results section contains additional information for each event returned by the search, including the timestamp, showing when the activity occurred, the IP address from which the activity was performed, the name of the user and the activity, the item in question, for example, a query result or a filename, and any additional details.

3. Select a column header under Results to sort by.

   Column|Definition
   ------|-----------
   Date |The date and time (in UTC format) when the event occurred.
   IP address |The IP address that was used when the activity from a device was logged. The IP address is shown in IPv4 or IPv6 address format.
   User |The user (or service account) who performed the action that triggered the event.
   Activity |The activity performed by the user. This value corresponds to the activities that you selected in the Activities dropdown list. For an event from the Exchange admin audit log, the value in this column is an Exchange cmdlet.
   Item |The object that was created or modified because of the corresponding activity. For example, the file that was viewed or modified, or the user account that was updated. Not all activities in this column have a value.
   Detail |Any additional detail about an activity. Not all activities have a value.

## View the details for an event

You can view more details about an event by selecting the event record in the list of search results. A Details page shows the detailed properties from the event record. The properties shown depend on the Office 365 service in which the event occurs. To view these details, select More information. For information about properties, see Detailed properties in the audit log.

 

Activities audited by Workplace Analytics
The following tables describe the file and page activities in Admin settings.
Admin activities
Name	Description
Uploaded org data	Admin uploaded organizational data file
Updated Privacy Setting 	Admin updated settings
Updated data access setting	Admin updated data access settings

Query Data Access Control (Analyst activities)
Name	Description
Executed Query	Ran a query
Cancelled Query	Cancelled a running query
Delete Result 	Deleted query result
Downloaded Report 	Downloaded query result
Accessed OData link	Accessed OData link
Create Meeting Exclusion 	User created a new meeting exclusion
Updated Preferred Meeting Exclusion	User updated preferred Meeting Exclusion

Explore data access
Name	Description
Viewed Explore 	Viewed Explore


Use PowerShell to search audit logs
You can also use PowerShell to access the audit logs based on your login. The following example shows how to use the Search-UnifiedAuditLog command to pull Workplace Analytics audit log entries.
To use the New-PSSession command, your account must have an Exchange Online license assigned to it, and you need access to the audit log for your tenant. For more information on connecting to Exchange Online, see Connect to Exchange Online PowerShell.

Set-ExecutionPolicy RemoteSigned

$UserCredential = Get-Credential

$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection

Import-PSSession $Session
Search-UnifiedAuditLog -StartDate 1/1/2019 -EndDate 1/31/2019 -RecordType WorkplaceAnalytics-ResultSize 1000 | Format-Table | More
