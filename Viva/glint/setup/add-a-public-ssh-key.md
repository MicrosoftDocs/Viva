---
title: Add a public SSH key to Viva Glint
description: To access your Microsoft Viva Glint SFTP account after SSH key pair generation, upload your public SSH key to Viva Glint.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: SFTP, public SSH key, upload SSH key
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 04/10/2023
---

# Add a public SSH key to Viva Glint

To access your Microsoft Viva Glint SFTP account after [SSH key pair generation](https://go.microsoft.com/fwlink/?linkid=2240226), upload your public SSH key to Viva Glint using the guidance below.

> [!NOTE]
> Do not share your private SSH key file with Viva Glint.

## Add a public SSH key

To import your public SSH key to Viva Glint:

1. From the admin dashboard, select the **Configure** symbol, then in **Client Settings** choose **Advanced Configuration**.
2. In the **Data Apps** menu, select **MANAGE\_SFTP\_KEYS\_SAPP**.
3. From the **Action** dropdown menu, select **Add SFTP public key.**
4. In the **Public Key** field, **paste** the contents of your SSH public key file.
   1. **Open** the SSH public key file in a text editor application (like Notepad) to **copy** the key.
5. Select **Show first 100 records** to upload the public key.
6. When successfully uploaded, a table will display the new public key and all other keys on file.

## Understand next steps

After successful public SSH key upload to Viva Glint, to test the connection to Viva Glint SFTP:

1. Confirm that all public IP address(es) for accounts that will connect to SFTP are added to Viva Glint General Settings.[Configure SFTP IP addresses in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2238339).
2. Use the credentials below to connect with a File Transfer Protocol (FTP) application:
   1. **File Protocol:** SFTP
   2. **Host name:**
      1. **US-based customers:** sftp.us1.glint.cloud.microsoft
      2. **EU-based customers:** sftp.eu1.glint.cloud.microsoft
   3. **Port**: 22
   4. **Username**: company ID
   5. **Password**: None.nSelect your private SSH key file to connect.