---
title: Integrate your HRIS with Viva Goals
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to provision users and teams automatically, and stay up-to-date with employee information at all times."
---

# Integrate your HRIS with Viva Goals

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to HRIS integration

Every workplace is subject to an ever-changing technological landscape, and oftentimes it becomes important to synchronize employee information across multiple tools managed by the HR department. Ideally, you'll want to import as much data as possible from your HRIS to other tools automatically, simply because importing the data manually is a time-consuming, and laborious process. 

The primary step in getting started with Viva Goals is onboarding users and teams to the system. You can automate this step using our integration with popular Human Resource Information Systems such as **SAP SuccessFactors**, **Workday**, **UltiPro**, **Gusto**, and **Rippling HR** among others, that fetches relevant information from your HRIS, and updates this information dynamically.

You can save yourself from the hassle of inundating your IT helpdesk with requests for **provisioning**, **deprovisioning**, or **updating employee information**. 

## How does the integration work?

Viva Goals’ HRIS integration works on the principle of **Secure File Transfer Protocol (SFTP)**. SFTP is a network protocol for file transfer that uses encryption algorithms to securely move data to a server, and makes the file unreadable during this process. Since authentication is involved in SFTP, unauthorized file access is prevented during the transfer process. This provides organizations a higher level of file transfer protection. There are two methods for authenticating connections — password authentication, and key authentication. Viva Goals uses **password authentication** wherein you can simply use the encrypted credentials provided by us to ensure a secure file transfer from your system to our server. 

The first step is to import employee data from your HRIS and drop this file at a secure location (which is our SFTP server). We'll fetch this file, and provision users and teams into your Viva Goals account automatically. The file location, and data during transfer is encrypted, ensuring top-notch security. 

To keep this information current, you can schedule a task that will automatically import personnel information from your HRIS, and drop this file to our server.  For example, once everyday at 9AM, the entire employee information should be exported, and saved in the specified file location. By doing this, for every user and/or team addition and/or deletion, or any updates, the information will be synchronized dynamically from your HRIS to Viva Goals.

## Format for importing user and team information

Ensure that the user and team file includes the exact labels of Viva Goals’ standard header fields, and the file should be in CSV format. 

**Users**
:::image type="content" source="../media/goals/goals-HRIS-users-template.png" alt-text="Image of user template ":::

**Teams**
:::image type="content" source="../media/goals/goals-HRIS-teams-template.png" alt-text="Image of teams template":::

## Points to be noted

1. The CSV file needs to be imported in the prescribed format. 

1. The header labels should be exactly the same as that of Viva Goals’ standard header labels. 

1. Custom field header labels should match any existing custom field in Viva Goals. 

1. New fields outside of Viva Goals’ standard fields or existing custom fields will be treated as new custom fields.

1. If a user’s email exists in Viva Goals, we'll update the information with the fields that match. We'll create new users only if the user’s email doesn’t exist in Viva Goals. 

1. If a team exists in Viva Goals with the same name as provided in the imported file, we'll update the information with the fields that match. We'll create a new team only if there's no team in Viva Goals that goes by the name provided in the imported file. 

1. In this process, we'll never remove any existing field value for both users & teams.

1. If a manager (who is mapped to a user) provided in the imported list isn't a user in Viva Goals, this user will be created as a manager in Viva Goals with the default values, and mapped to the user automatically. 

1. If a team (that is mapped to a user) provided in the imported list isn't a team in Viva Goals, this team will be created in Viva Goals with the default values, and mapped to the user automatically. 

1. If a specified parent team isn't present is Viva Goals, a new team will be created with the default values, and will be mapped as the parent team in Viva Goals. 

1. If a user's deactivation date is before the date of import, the user will be deactivated 24 hours after the import. 

1. Supported date formats are (dd/mm/yyyy) or (mm/dd/yyyy). 

1. If a user is omitted from a file, this won't remove the user from Viva Goals.

## User field validation

- **User Emai**l has to be unique and mandatory. All other fields are optional. 

- **User Name** can be provided as a single field 'User Name' or can be given as 'First Name' and 'Last Name' in two separate columns. 

- **Teams** can have a comma-separated list if the user belongs to multiple teams.

- **Is Org Admin** is a Boolean field and should have a 'Yes' if the user in your organization is an admin or a 'No' if the user isn't an admin.

- **Deactivation Date** accepts date in the format: mm/dd/yyyy or dd/mm/yyyy and the user will be deactivated on the specified date. 

## Custom field for users

Viva Goals will consider all the headers other than the default ones as custom fields for the user. When the feed from your HRIS provider has these custom fields, we'll add these automatically to the user record. For example, Employee ID, Joining Date, and likewise. 

Custom fields for users will be treated as text fields, date, or boolean fields as per the format. While exporting users in Viva Goals, all the custom fields will be included.

## Team field validation

- **Team name** should be unique and mandatory. 

- The organization owner will be assigned as the **Team Owner** if the team owner information is not provided in the file.

- **Parent Team** should have the name of the parent team.

- **Team Type** is an optional text field.  

## How to enable SFTP integration?

HRIS integration is available only for Enterprise customers. If you would like to have this enabled for your organization please reach out to support@vivagoals with the request. Alternately, you can reach out to your CSM to have this enabled for your organization. 

Here's how the setup process would look like if you decide to enable the SFTP integration with Viva Goals:

1. Once you reach out to your CSM, the team at Viva Goals would create the folder and host it. (If you prefer Viva Goals to host the file.)

2. Once the folder is created, the credentials for that SFTP folder will be shared with your organization's representative. Using these credentials, you would be able to access that folder. 

    ```al
    Sample information
        
        Mavericks
        Organization ID: 007
        Host: [host_url]
        Username: Mavericks_007
        Password: $$$$$$$$
    ```

    > [!NOTE]
    >  If you choose to host the SFTP folder, then we would require you to share this information with us in order to contact the folder. The other steps below remain the same. 

3. The next step would be to share a sample file of users or teams for your organization. [Refer to the format](https://help.ally.io/en/articles/3669172-integrate-your-hris-with-ally-io#format-for-importing-user-and-team-information) that we're expecting for users and teams. Note that if the headers are different, we can map your headers to ours in the backend but the values that we expect need to be in the format as shown [here.](https://help.ally.io/en/articles/3669172-integrate-your-hris-with-ally-io#format-for-importing-user-and-team-information)  

4. The Viva Goals team will configure your folder credentials in the backend while we verify the format of the files you share.

5. Before you can start dropping the files in the SFTP folder, we would require the email recipients who would require to be notified when SFTP uploads happen and also the frequency at which you would like us to pull the data from the SFTP folder into Viva Goals. 

    > [!NOTE]
    > The email recipients would need to be users of Viva Goals in order to receive SFTP updates. Any email address that is not associated with any user in Viva Goals will not be able to receive these notifications. 

6. Once the email recipients and the sync frequency are configured, you can drop the files into the SFTP folders and the sync will happen. 

## Common Questions

### 1. Can I use my SFTP server instead of one hosted by Viva Goals?

Viva Goals can create the SFTP server location that’s hosted by us to drop files or can use any existing SFTP server that’s hosted by your organization. 

### 2. What is the supported file format?

Both the user & team import files should be UTF-8 encoded. 

### 3. When does the user and team data synchronize? 

The user & team import will happen once a day for every organization. Please reach out to support@XXXX or your CSM to better understand the schedule. 

### 4. How to export users?

On the top-right corner of the tabular summary, you'll find an option to export users. A mail will be sent to the administrator for downloading the report.

:::image type="content" source="../media/goals/goals-admin-users-export.png" alt-text="Image of admin users export":::

### 5. What happens if a previously imported Viva Goals user no longer appears in a new CSV upload?

- If a user is omitted from a file, this will not remove the user from Viva Goals.

- The users remain as is, there is no change or addition/deletion taking place in this case.

- The user is not disabled and the user account is left in its original state.

### 6. What happens if a Manager’s account is deactivated? Do people under the manager have their “Manager Email” field changed automatically, or is it left alone?

- The Manager goes into the Deactivated state.

- Users under the Manager retain the same Manager Name in Viva Goals.

- The Manager field for the employees reporting to this manager will be updated only if the Manager Email field is set in the import file.


### 7. When setting up a team hierarchy for a user, does Viva Goals assign the user to all parent teams of the mentioned Teams?

- Only the Teams mentioned in the User Import template against the entry for the user will be considered as the team(s) that the user is part of.

- For example, if the import file contains the user as a member of only the Sub Admin team, then the user will not be a part of Admin A and Administration unless both of those parent teams are added in the import file for the user.

:::image type="content" source="../media/goals/goals-admin-add-teams.png" alt-text="Image of admin add teams":::

### 8. What happens if a Team name changes between uploads?

A new team gets created and the user gets added to that team.

The old team doesn't get deleted.

### 9. If I leave the Is Org Admin field blank for a current Org Admin, will that remove the Org Admin status?

The user retains their Org Admin role even if the field is left blank for their row.

User will be removed from the Org Admin role ONLY IF the Is Org Admin field is set to No.

### 10. What happens if a user who doesn't currently exist in Viva Goals is uploaded with a deactivation date in the past?

A new user account is created but is in the Deactivated state. 