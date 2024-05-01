---
title: Import members into a Viva Glint Distribution List 
description: Importing members into your Viva Glint HRIS file is easy and you can also take advantage of the blended membership Distribution functionality.
ms.author: alanderfield
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Removing attribute rules,
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high pri
ms.date: 09/07/2023
---

# Import members into a Viva Glint Distribution List 

Importing members to an existing Distribution List removes the current attribute rules from that list.

## Imports can be into a .csv or .xlsx file

Follow this procedure:

1. From the **Distribution Lists** page, select the existing list you want to make additions to.
2. Select the **Add/Edit Employees** button.
3. From the **Choose a way to add employees** window, select **Import**.
4. Choose .csv or .xlsx file.
5. Drag and drop or browse to upload a file (maximum size 50 mb).
6. Select **Import File**.
7. The **Confirm your import** window displays. View the summary and if it's as expected, select **Confirm Import**.

> [!TIP]
> [Read this guidance for more information to set up and use Distribution Lists in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2246615)

## Optional - Use the blended membership Distribution List functionality

Dynamic attributes automatically add and remove users to and from a distribution list. They can also include or exclude certain users from a list. Knowing how your distribution list has been populated helps you make decisions about how to add users.

### View how a Distribution List was populated

From the **Distribution Lists** page, the far-right column entitled **Membership Type** defines if the list in that row has been populated manually, by attribute rules, or both.

> [!NOTE]
> If a distribution list is populated by an Import, it will have the membership type "manual".

## Use the dynamic Distribution Lists functionality

Your decision whether to use manual population or attribute rule population should be guided by these principles:

- If membership type is based on **Attribute Rules** and a user is manually added in the platform, employee data file imports (i.e. Rubicon) will automatically update the Distribution List.
- If the Distribution List began manually, adding attribute rules will change the list to include both **Attribute Rules** and **Manual**.
- If a manually added member is deleted and they match the filter criteria, they'll still appear in the Distribution List, but the **Added by** method will change from **Manual** to **Attribute Rules**.

    > [!IMPORTANT]
    > Importing users to an Attribute Rules Distribution List removes existing rules.
    >
    > - Activate the **Preserve the employees already in this distribution list**  functionality to convert membership type to **Manual** for existing users.
    > - Uncheck to deactivate and remove the users based on the rules, and only include those in the import file.
