---
ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics data export steps
description: Learn about Workplace Analytics Data export and how to use it for advanced data analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Workplace Analytics Data export

_Data export is only available as part of a Microsoft service engagement._

Your company might have unique data-analysis needs requiring custom exploration of Workplace Analytics insights and data that goes beyond what's available in Workplace Analytics. For example, you might have custom data exploration that requires you to combine Workplace Analytics data with data outside of Workplace Analytics.

After you get a CS agreement, you can ask your Microsoft representative to enable data export for your Microsoft 365 tenant.
<!--You can also specify which partition to enable data export for in the Workplace Analytics app. The ability to specify what data can be exported by whom helps you maintain data protection.-->

After data export is enabled, your Workplace Analytics admin can view and use the Data export page in Workplace Analytics to save the SAS URI, which points to an Azure storage container with write-only permission.

Saving the SAS URI enables a workflow that exports the Workplace Analytics data to the storage container. The data will be exported each time it is refreshed in Workplace Analytics, for the agreed duration of the CS agreement.

## Data included in the export

You can export pre-processed Workplace Analytics data to a designated Azure storage container as .csv files. The export uses the latest available organizational data that was uploaded and processed in Workplace Analytics.

If you add new organizational data attributes to your Workplace Analytics upload, you must also add them as additional fields that you want to include in the export in the **Field privacy** section on the **Data export** page. The new fields are added to the next data export after the data upload is next refreshed and processed in Workplace Analytics. For details, see [Upload organizational data (subsequent uploads)](../setup/upload-organizational-data.md).

The following .csv files are included in data exports. Select a file to view what's included in that file, such as the data column names, data types, and definitions:

* [Meetings](./Meetings.md)
* [MeetingParticipants](./Meetingparticipants.md)
* [PersonHistorical](./PersonHistorical.md)
* [MailParticipants](./MailParticipants.md)
* [Mails](./Mails.md)
* [Calls](./calls.md)
* [CallParticipants](./callparticipants.md)
* [InstantMessages](./instantmessages.md)
* [InstantMessageParticipants](./instantmessageparticipants.md)

## Azure environment requirements

Before exporting Workplace Analytics data, confirm the following: 

* Your company has a current Azure subscription and an Azure storage account with an Azure storage container for storing the exported Workplace Analytics data.

* Have a write-only SAS URI for the storage container. To learn more about SAS, see [Delegating Access with a Shared Access Signature](/rest/api/storageservices/delegating-access-with-a-shared-access-signature).

## To export data from Workplace Analytics

1. If you have already installed Azure Templates, use the SAS URI created after deployment which grants write-only access to the raw data folder that was set up during deployment and use that URI in **Step 3**.
2. In Workplace Analytics, go to **Settings** > **Data export**.
3. In **Azure storage container SAS URI**, enter the URI for the Azure storage container.
4. In the **Field privacy** section, select which fields to export as raw values and as hashed values. Note the options for the required fields at the top of the list are locked and unchangeable, as shown in the following graphic.

   >[!Note]
   >When you add new attributes to your organizational data and you want to include them in a data export, you must repeat this step to add the new attributes as additional fields to include in the export.

5. Select **Save** (top right) to save your selections and enable a workflow that exports the Workplace Analytics data to the storage container. The applicable data is then exported to Azure during each subsequent data refresh in Workplace Analytics.

   ![Workplace Analytics data export settings page](./images/data-export.png)
