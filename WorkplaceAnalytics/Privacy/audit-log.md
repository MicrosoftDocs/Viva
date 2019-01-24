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

* To access the auditing section of the Office 365 Security & Compliance Center, you must have an Exchange Online license (included with Office 365 Enterprise E3 and E5 subscriptions).
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

