---
title: Set up attribute-based survey access in Viva Glint 
description: Microsoft Viva Glint's attribute-based survey access allows users without a corporate email account to complete confidential surveys. 
ms.author: JudithWeiner
author: JudyWeiner
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: variables & product text, attribute-based URL, survey access 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/08/2024
---

# Set up attribute-based survey access in Viva Glint

Microsoft Viva Glint's Attribute-based Survey Access allows users without a corporate email account to complete confidential surveys using attribute-based survey access, which is designed for mobile or public devices including desktops, laptops, tablets, or mobile phones. Users access surveys using key identifiers. These identifiers ensure a user's responses are tied to their survey and allow for full reporting on demographics in survey results.

## Understand key identifiers

Viva Glint uses key identifiers to uniquely identify each user. Because these users may not have email addresses, attribute-based survey access requires the use of two attributes - the combination known only to the specific user. The system is flexible enough to support any two attributes that are a part of your employee data file:

- One of these attributes is always a unique identifier
- The other attribute should be something not commonly known, like the employee ID number or birth year.

## Set up attribute-based survey access

### Configure General Settings

1. From the admin dashboard, select the **Configuration** symbol, then in **Client Settings**, choose **General Settings**.
2. In the **All Settings** menu, select **Engage Survey Details**.
3. Next to **Attribute-based Survey Access,** select **Set up**.
4. In the **Attribute-based Survey Access** pane, turn on the **Enable when ready** toggle.
5. If desired, edit the **Welcome text** or **Instruction text** fields by entering new text.
6. Select **+ Add an attribute** and select attributes from the dropdown menu.
   > [!NOTE]
   > Complete attribute setup and employee data upload prior to selection for attributes to be available.
7. Edit the **Placeholder text** that displays under each selected attribute.
8. Confirm your edits in the **Preview** at the bottom of the pane.
9. At the top of the pane, select **Save**.
10. Select the Configure symbol, then in **Service Configuration**, choose **Advanced Configuration**.
11. In the **Details** section, confirm that the **Enable Kiosk Page** checkbox is selected. If not, select this checkbox.
12. Select **Save Changes** at the bottom of the **Details** page.

### Manage translations

To add translations for your organization's survey languages, use the dropdown menu in the **Attribute-based Survey Access** setup section or import translations using the **Variables & Product Text** feature.

> [!NOTE]
> The language selection dropdown menu on the Attribute-based Survey Access survey landing page includes all languages in that your organization selects in General Settings as Supported Survey Languages. The languages available aren't limited by what's selected in the survey program.

#### Use the language dropdown menu

1. In the Attribute-based Survey Access setup pane, select a language from the **Language:** dropdown menu.
2. Add translations to the Welcome Text, Instruction Text, and the Placeholder text fields.
3. Select **Save** and repeat for each language.

#### Use the Variables & Product Text

1. Go to **Configuration** and in the **Service Configuration** section, select **Variables & Product Text**.
2. In the dialog that appears, select **Export Product Text** and in the next dialog, select languages in the **Languages to Include** field.
3. Select **Export** to download a compressed folder (.zip) to your device.
4. The exported folder contains a .csv file for each language. **To preserve special characters, open each .csv file by [importing them to Excel](https://support.microsoft.com/office/import-data-from-a-csv-html-or-text-file-b62efe49-4d5b-4429-b788-e1211b5e90f6).**
   > [!IMPORTANT]
   > To prevent import errors, don't change the file names or column labels in the exported files.
5. Each file contains three fields. Add translations to the **VALUE** column for each field.
   
   - PULSE_LOGIN_PAGE_DESCRIPTION
   - PULSE_LOGIN_PAGE_FIELD_1
   - PULSE_LOGIN_PAGE_FIELD_2
  
   > [!IMPORTANT]
   > PULSE_LOGIN_PAGE_FIELD_1 corresponds to the first attribute listed in the Attribute-based Survey Access setup pane PULSE_LOGIN_PAGE_FIELD_1 corresponds to the second attribute listed. Ensure that translations are entered for the correct attribute.
  
6. After entering translations, save each file as .csv with the same naming convention as the exported files. For example: textSnippets_202408221_121422_es_US_Spanish (Americas).csv.
7. After editing and saving all files, compress them into a .zip folder.
8. Go to **Configuration** and in the **Service Configuration** section, select **Variables & Product Text**.
9. Select **Import Product Text**.
10. In the dialog that appears, drag and drop your .zip file or browse to choose it on your device.
11. In the **Confirm your languages** dialog, verify that the listed languages match the files you imported.
    1. If something isn't correct, use the language dropdown next to a file to change the language.
12. Select **Next**.
13. In the **Import Product Text CSV or ZIP** dialog that appears, verify that the upload summary is correct and select **Make Changes**.
14. Return to the Attribute-based Survey Access setup section and select languages from the dropdown menu to confirm that updates applied.

### Get the attribute-based survey access URL

1. From the admin dashboard, select the **Configuration** symbol, then in **Surveys**, choose **Survey Programs.**
2. Select the survey program that should have attribute-based survey access.
3. At the top of the page, select **Copy survey link,** and then **Copy** in the dialog.
4. Optionally, use online tools to convert this link into a QR code or shortened link for easy participation on mobile devices.

> [!NOTE]
> If users become INACTIVE during a survey, they're still able to access surveys with attribute-based access.

