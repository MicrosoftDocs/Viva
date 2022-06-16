---
title: Yume - Overview
description: Learn about Yume, the solution the employees use to manage their interactions with their managers
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Yume - Overview and setup

Yume is an employee-driven solution to support 1:1 interaction between employees and their managers. It empowers employees to shape 1:1 meetings through topics (cards) that make discussions more meaningful. Employees can build and structure the agenda for an upcoming 1:1 meeting using the cards, which contain content that is simple and easy to access during the meeting. The employees can also refer to cards and key notes from previous 1:1 meetings and prepare cards for the future 1:1 meetings, promoting continuity and evolution of 1:1 meetings. There's also an option for employees to provide their feedback on the 1:1 interaction immediately once the meeting ends.

## Use case

1.	An employee has a challenge (for example, work-life balance and personal situation) that they want to bring up to their manager, but is unsure how to.
2.	An employee wants to explore, discuss and/or focus on their career growth and development.
3.	An employee is a new hire and wants to build a relationship with their new manager.

## Prerequisites for setup of Yume

To set up Yume, perform the following steps:

- Clone the [VivaSolutions GitHub repository](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions) onto the machine in your location, and download the Yume accelerator from the samples in this repository.

> [!NOTE]
> You can choose to clone the repository or download the Yume accelerator from the samples of the repository directly from the server itself.

Using these samples, perform the following substeps:
- Create an Azure AD Application registration.
- Import the PowerApps Custom Connector.
- Create Dataverse tables and permissions.
- Import data into the Dataverse table.

### Create an Azure AD Application registration

Create an Azure AAD Application registration by performing the following steps:

1. For the attribute **Name**, provide the value **vsol-yume-connector**.
1. Configure the following delegated permissions for the "Microsoft Graph" API:
    - Analytics.Read
    - MailboxSettings.Read
    - User.Read
    - Profile
1. Authenticate using the Web Redirect URL: https://global.consent.azure-apim.net/redirect
1. Create a client secret and make a note of its value.
1. Make a note of the Application ID (also known as the client ID).
   The value of the client secret and the client ID will be used during the PowerApps Custom Connector creation.

### PowerApps Custom Connect import

To import the PowerApps Custom Connector, perform the following steps:
1. Sign in to powerapps.microsoft.com.
1. Select **Data** (or **Dataverse**) on the left navigation menu.
1. Select **Custom connectors**.
1. Choose **+ New custom connector**.
1. For the **Connector name** field, enter **vsol-graph-analytics-connector**.
1. Select **Import**.
1. Select the *vsol-yume-connector.swagger.json* file and select **Open**. The **General** page that is displayed.
1. Leave all the values as is and click **Security**. The **Security** page is displayed.
1. On the **Security** page, perform the following substeps:
    1. For the **Client ID** field, enter the client ID (application ID) from the Azure AAD application registration process.
    1. For the **Client secret** field, enter the client secret value from the Azure AAD application registration process.
    1. For the Resource URL field, enter **https://graph.microsoft.com**.
    1. For the Scope field, leave the populated value as is.
    1. Select **Create connector** at the top-right of the menu-items bar.
    1. Select **Close** at the top-right of the menu-items bar. The connector should now be listed in the **custom connector** section.
1. Share the connector with the organization (as needed).

### Create Dataverse tables

1. Create the Dataverse tables that are described below. For more information on creating Dataverse tables, see [Create a custom table](/power-apps/maker/data-platform/data-platform-create-entity).

**Yume cards**


|Column |Description  |
|---------|---------|
|TitleId     |   **Whole number**: Unique ID for the Title and Suggestions      |
|TitleName     |    **Text (850)**: (Primary column, Option Required) Title for the main category (needed only for the title card)     |
|TitleType     |**Text (100)**: Defines what the TitleName will be used for;               **MainTitle**: Identify TitleName as the main card title; **ContentTitle**: Identify the TitleName as the title for the content. |
|TitleContent     |   **Text (2048)**: Content for the card      |
|ContentType     |   **Text (100)**: Defines what the TitleContent will be used for;               **MainTitle**: Identify the TitleContent as the Description content for the main card title; **ContentTitle**: Identify the TitleContent as the content of the main card.      |
|CardType     |     **Text (100)**: Identifies how the display area content for the card will be presented.            **Metrics**: Predefined Viva Personal Insights based on graph data; **Horizontal**: Left/right control for navigating the content for the main card; **Vertical**: Vertical gallery (list) display of the content.  |
|DisplayOrder     |     **Whole Number**: The order to display the content in the horizontal/vertical format.    |

**Yume Meeting Notes**


|Column  |Description  |
|---------|---------|
|MeetingId     |    **Text (512)**: (Primary) Outlook meeting ID     |
|MeetingDateTime     |     Date and time    |
|MeetingName     | **Text (1024)**: Outlook meeting subject line        |
|MeetingTasks     |   **Text (2048)**: Delimited task list      |
|CaIds    |     **Text (1024)**: Delimited card IDs    |
|Emp Feedback     |    **Text(1024)**: Emp meeting feedback     |
|Emp Feeling     |      **Text(100)**: Emp meeting sentiment   |

**Yume User Options**


|Column  |Description  |
|---------|---------|
|SettingName     |    **Text(100)**: (Primary) Setting Name     |
|SettingValue     |   **Text (512)**: Content for the card      |

2. During the Dataverses table creation, make a note of the table prefix name.

### Create Dataverse permissions

To create Dataverse permissions, perform the following steps:

1. Launch the URL https://admin.powerplatform.microsoft.com/environments. 
1. Select the environment for which you want to create Dataverse permissions.
1. Select **Users and permissions > Security Roles**.
   The following roles are the ones you can create:
    - Basic User role (for access to User table and Yume tables): Updated to include user rights for tables. This role provides read-only access for the card data table but additional rights for the other yume tables.
    - YumeContentAdmin (custom role): This role is permissive so should only be accounts that need access across all the data (for example, nudges from power automate).
        - Yume Cards::: Parent: Child Business Units
        - Yume Meeting Notes ::: Parent: Child Business Units
        - Yume User Options ::: Parent: Child Business Units
         
       Members of this role will get the permissions as depicted in the following screenshot:
 
### Set working hours and days for users mailbox settings

For information on how to set working hours and days for user mailbox settings, see [Set-MailboxCalendarConfiguration](/powershell/module/exchange/set-mailboxcalendarconfiguration).

### Publish the Yume application to the organization app catalog

For more information on how to publish the Yume application to the organization app catalog, see [Embed a canvas app as personal app in Teams](/power-apps/teams/embed-teams-app).

## Create the Power Automate flows for nudging

To create the Power Automate flows for nudging, perform the following steps:
1. Download Task and Meeting zip file.
1. Create a service account (as needed).
1. Add the service account as a member of the YumeContentAdmin security role.
1. Sign in to PowerAutomate y launching the URL https://powerautomate.microsoft.com.
1. Create connections to **Teams** and **Microsoft Dataverse**, for example, adding connections for Microsoft Dataverse.
1. Import the meeting flows by performing the following substeps:
    1. Select the resource types for Microsoft Dataverse Connection and Microsoft Teams Connection.
    1. Select **Create as new** (update the name as needed).
       > [!NOTE]
       > If an error is displayed, select **Save as new flow**.
    1. Update the **Initialize variable** page for dataprefix by performing the following substep:
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot:
    1. Update the **Initial variable** page for yumeurl by performing the following substep:
        1. Populate the **Value** field with the value of the powerapps Weblink URL for the Yume powerapp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.
1. Repeat the import process for the Tasks flow by performing the following substeps:
    1. Update the **Initialize variable** page for dataprefix by performing the following substep:
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627**.
    1. Update the **Initial variable** page for yumeurl by performing the following substep:
        1. Populate the **Value** field with the value of the powerapps Weblink URL for the Yume powerapp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.
