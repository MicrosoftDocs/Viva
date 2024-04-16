---
title: Set up attribute-based survey access in Viva Glint 
description: Microsoft Viva Glint's attribute-based survey access allows users without a corporate email account to complete confidential surveys. 
ms.author: JudithWeiner
author: JudyWeiner
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: variables & Product text, attribute-based URL, survey access 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 04/15/2024
---

# Set up attribute-based survey access in Viva Glint

Microsoft Viva Glint's Attribute-based Survey Access allows users without a corporate email account to complete confidential surveys using attribute-based survey access, which is designed for mobile or public devices including desktops, laptops, tablets, or mobile phones. Users access surveys using key identifiers. These identifiers ensure a user's responses are tied to their survey and allow for full reporting on demographics in survey results.

## Understand key identifiers

Viva Glint uses key identifiers to uniquely identify each user. Because these users may not have email addresses, attribute-based survey access requires the use of two attributes - the combination known only to the specific user. The system is flexible enough to support any two attributes that are a part of your employee data file:

- One of these attributes is always a unique identifier
- The other attribute should be something not commonly known, like the employee ID number or birth year.

## Set up attribute-based survey access

### Configure General Settings

1. From the admin dashboard, select the **Configure** symbol, then in *Client Settings*, choose **General Settings**.
2. In the *All Settings* menu, select **Engage Survey Details**.
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
11. In the **Details** section, select the **Enable Kiosk Page** checkbox.
12. Select **Save Changes** at the bottom of the Details page.

### Obtain the attribute-based survey access URL

1. From the admin dashboard, select the **Configure** symbol, then in *Surveys*, choose **Survey Programs.**
2. Select the survey program that users will complete with attribute-based survey access.
3. At the top of the page, select **Copy survey link,** and then **Copy** in the dialog box.
4. Optionally, use online tools to convert this link into a QR code or shortened link for easy participation on mobile devices.

> [!NOTE]
> If users become INACTIVE during a survey, they're still able to access surveys with attribute-based access.

