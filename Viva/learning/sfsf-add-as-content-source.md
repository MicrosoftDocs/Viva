---
title: Add SAP SuccessFactors as a content source
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 02/26/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Configure SAP SuccessFactors as a learning content source for Microsoft Viva Learning.
---

# Add SAP SuccessFactors as a content source

This article shows you how to configure SAP SuccessFactors as a third-party content source for Microsoft Viva Learning. First, you'll need to edit the system configuration in the SuccessFactors Portal, and then you'll need to complete the configuration in the Microsoft 365 admin center (MAC).

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. SAP SuccessFactors content and any associated services are subject to the SAP SuccessFactors privacy and service terms.

## Create your PGP pair key to enable integration

Use a PGP tool to generate a PGP key (public key, private key, private key passphrase) to enable this integration. 
We recommend using the Kleopatra tool, which can be downloaded at [Gpg4win](https://www.gpg4win.org/). Follow the guidelines on [GNU Privacy Guard](https://gnupg.org/).

### PGP key generation instructions for Windows

1. Download the Kleopatra tool from [Gpg4win](https://gpg4win.org).

1. Open Kleopatra. Navigate to **Certificates** > **New Key Pair**.

   ![Image of the Kleopatra tool home screen.](../media/learning/sfsf-kleopatra-1.png)

1. Enter your name and email, and then select “Protect the generated key with a passphrase.”

   ![Image of login window in Kleopatra prompting name and email credentials.](../media/learning/sfsf-kleopatra-2.png)

1. In **Advanced Settings**, change **Key Material** to **RSA**.

   ![Image of Advanced Settings with Key Material selected as RSA in Kleopatra tool.](../media/learning/sfsf-kleopatra-3.png)

1. Select **OK** to generate your key pair.

1. Enter a passphrase for your key pair and note this for future reference in the Microsoft 365 admin center.

   ![Image of prompt to enter passphrase to protect your new key in Kleopatra.](../media/learning/sfsf-kleopatra-4.png)

1. Navigate to **File** > **Backup Secret Key**. Save your secret key locally for future reference.

   ![Image of file menu with Backup Secret Keys option selected.](../media/learning/sfsf-kleopatra-5.png)

1. Navigate to **File** > **Export**. Save your public key file locally for future reference.

You've now successfully generated and saved your public and private key pair.

### PGP key generation instructions for UNIX and Linux systems 

1. Download [GNU Privacy Guard](https://www.gnupg.org/).

1. On the GnuPG website, go to **Documentation**, then choose **Guides**.

1. Open the GNU Privacy Handbook.

1. Follow the instructions in the section **Generating a new keypair**.

## Configure in your SuccessFactors portal

>[!NOTE]
>You'll need to have admin permissions in SuccessFactors to complete these steps.

1. Enter "Learning Administration" in the search bar on the SAP SuccessFactors portal, and then select the enter key.

   ![Image of SAP SuccessFactors Portal where you search for Learning Administration.](../media/learning/SFSF-admin-center-page.png)

1. Get the required workflows to edit the PARTNER_EXTRACT configuration located at **System Administration** > **Configuration** > **System Configuration** > **PARTNER_EXTRACT**.

   ![Image of System Configuration meny with option section in PARTNER_EXTRACT.](../media/learning/sfsf-system-config-partner-extract.png)

1. Fill in the following parameters in the PARTNER_EXTRACT configuration. To edit the partner extract configuration in SuccessFactors, you'll need **Edit System Configuration** workflow permission in SuccessFactors.
![Image of SAP SuccessFactors Learning System Configuration screen with partner extract field highlighted.](../media/learning/SFSF-system-config-highlighted-1.png)   
   Edit the following fields: 
   - **#customer notification email for all job status** </br></br>
             **defaultJob.email=**
       Enter the email address in the following format: 
        `defaultJob.email=johndoe@contoso.com` 
     -  For Microsoft Viva Learning, enter the value **MVL**.
         - partners1.partnerID=
         - Correctly formatted line should read like this: `partners1.partnerID=MVL`
         -  EncryptionKey is the PGP public encryption key.
   >[!NOTE]
   > Don't copy over the header “BEGIN PGP PUBLIC KEY BLOCK” or the footer “END PGP PUBLIC KEY BLOCK”.  Only copy the key block, which should be a Base64 string. Then remove the new line characters after every line.

  - Correctly entered line should read like this example:   
         ```partner1.encryptionKey=mQGNBGNQnd0BDADTFw7G/NmYjT53GlLudCzrk7GPpsoav
            v3bkJZfqf26Gzb8hYXiT9vj4Q9L/x51LDJPzoqI4Q6gMxjqUM2K/v0Sge+Mw/B1w7zfg
            O7Sa5+UvFNN8xUHOfeZ+zSR+0f8aeC9j9Lt4QlDFnV8cdVHqmhAfnobOYvjFV7MrhgQ0
            65+IYrhnWgX9pyHEtsu3SCCFj74Etzv56gs4TGu0g/+5WVDH7Fbb0X5lvpVi+EwAwHHH
            DGK18BuPRWz1QTTTKdWAEfAlYd74P1p6Cafi5hhQYr9A+XKeh1msXC6wf+qm/drMR8Dh
            MGqxYwzuTZJbgn3Mac1P3oeTbam+eBxPTylxVB0q8fQdDZEUd5UbRNnbS+KSkhilPS9D
            RO3AYlCpo4YQrjVg0Smh8p8n3tpv+vSlKXyrTqxJTclnMAWNMHZlgA8AShmqpMKcTglP
            dbl3YrP4Lhagj65KrlYLKiyBmzBttW+sZA5Fj4XVFZxNPzpJ6XuR5zbiU0JoeI7RdrI2
            C2als8AEQEAAbQjSm9obiBNaWdoZWxsIDxqb21pZ2hAbWljcm9zb2Z0LmNvbT6JAdcEE```

      - Key Owner maps to the User-ID of public key 
         - partners1.keyOwner= 
         - Correctly formatted line should read like: 
             - `partners1.keyOwner=John Doe <john.doe@contoso.com>`
   - Enable the partner extract by setting the field to true.
        - partners1.enabled=
   - Correctly formatted line should read like:
       - `partners1.enabled=true `
             
:::image type="Content" source="../media/learning/SFSF-system-config-highlighted-2.png" alt-text="Image of SAP SuccessFactors Learning System Configuration screen with partner1.enabled set to **true**." lightbox="../media/learning/SFSF-system-config-highlighted-2.png":::

After you've completed these steps in the SuccessFactors portal, you'll need to complete the setup in the Microsoft 365 admin center.

>[!NOTE]
>After you've finished the configuration in your SuccessFactors portal, SuccessFactors will generate the initial sync package. This may take up to 7 business days. Once the package is available in your SFTP folder path, Viva Learning will be able to begin communicating with SuccessFactors. If you can't find the package, contact your SuccessFactors support team.

## Configure in your Microsoft 365 admin center

>[!NOTE]
>You'll need to have admin permissions in Microsoft 365 to complete these steps.

### Prerequisite for configuration

Make sure that the SuccessFactors package is available in the SFTP folder path.

To obtain the folder path:

1. Navigate to **SF Admin Application** > **System Administration** > **Configuration** > **System Configuration** > **PARTNER_EXTRACT**.

1. Get the value of the defaultFtp.path property.

   >[!NOTE]
   >It may take up to 7 business days after configuration in your SuccessFactors portal for the SuccessFactors package to appear in your folder path. If you're still unable to find the package, contact your SuccessFactors support team.

### Admin center configuration

1. Navigate to your [Microsoft 365 admin center](https://admin.microsoft.com).

1. Navigate to **Settings** > **Org settings**. Search for *Viva Learning* and enable SAP SuccessFactors from the options.

1. Fill in the configuration details:
   - **Display Name**: Enter the display name you want to appear for the SAP SuccessFactors carousel.

   - **SFTP Host URL**: Navigate to **LMS Admin Application** > **System Administration** > **Configuration** > **System Configuration** > **CONNECTORS**. Get the value of the `connector.ftp.server` property.
   
   - Validate SFTP url, username and password by visiting https://<sftp_url> and logging in using username and password. 

   - **User Name**: Follow the same steps you followed for the SFTP Host URL. Get the value of the `connector.ftp.userID` property. Ignore the password available in the configuration site.

     :::image type="content" source="../media/learning/sfsf-system-config-highlighted3.png" alt-text="Image of System Config screen on connectors calling out admins to not enter the password in the connector.ftp.password field." lightbox="../media/learning/sfsf-system-config-highlighted3.png":::

   - **Password**: Check with your LMS application owner for help with retrieving your password. Enter that password here.

   - **Folder Path**: Navigate to **Learning Administration** > **System Administration** > **Configuration** > **System Configuration** > **PARTNER_EXTRACT**. Get the value of the `defaultFtp.path` property.
    
   - Validate the existence of the folder path in the SFTP server. Create the folder if it doesn't exist.

   - **Client's Host URL**: This is the BizX domain URL. You can get this from your BizX sign in URL. For example, if your BizX login URL is `organization.successfactors.com/sf/start/#/login` then the host URL is `organization.successfactors.com`.

   - **Client's Learning Destination URL**: You can get this from the learning domain module URL. For example, if the learning domain URL is `organization.scdemo.successfactors.com/learning/...` then the Learning Destination URL is `organization.scdemo.successfactors.com`.

   - **PGP Private Key**:private key for decryption. Don't copy over the header “BEGIN PGP PRIVATE KEY BLOCK” or the footer “END PGP PRIVATE KEY BLOCK”. You’ll need to copy the key exactly as it’s been generated; don’t remove new line characters. Only copy the key block, which should be a Base64 string.  

   - **PGP Private Key Passphrase**: You'll need to get the private key value from your IT admin or the team that provides your PGP key.

   - **PGP Public Key**: You'll need to get public key value from your IT admin or the team that provides your PGP key. 
      >[!Important]
      > - Don't copy over the header “BEGIN PGP PUBLIC KEY BLOCK” or the footer “END PGP PUBLIC KEY BLOCK”. You’ll need to copy the key exactly as it’s been generated. 
      > - Don’t remove new line characters. Copy only the key block, which should be a Base64 string.  

   - **Company ID**: Sign in to your SuccessFactors portal. Select your profile icon, then select **Show Version Settings**. You can view your company ID here.

      ![Image of the profile icon with Show Version Settings selected.](../media/learning/sf-3.png)

      ![Image of the version settings pane.](../media/learning/sf-1.png)

1. Select **Save** to activate SuccessFactors content in Microsoft Viva Learning. There may be a delay before the content is available in Viva Learning.

1. Close out of the Viva Learning flyout and re-open it. \
   If there are any issues, an error message will appear on the screen. \ 
   To troubleshoot the error, close and re-open the flyout. Select the learning source you're trying to enable. Check the specific error fields.

If an invalid Private and Public Key pair has been entered in the Microsoft 365 Admin Center (MAC), this error will display: "PGP Keypair validation failed. Possible reasons for this failure - 1. Incorrect values entered for fields -  SF Public Key, SF Private Key, SF Private Key Pass Phrase 2. PGP keys generated with incorrect algorithm.”

>[!Note]
> SuccessFactors courses will start appearing in Viva Learning within 7 days of successful setup.
Package generation from Success Factors takes up to 7 days. Once the package is generated, ingestion will be triggered and it will get completed within few hours based on package size.

SAP SuccessFactors deletes the Full Sync package from SFTP location automatically after 14 days from generation date.

All users within an organization will be able to discover all the tenant-specific courses, but they'll only be able to access and consume courses that they have access to. User specific content discovery is planned for future releases. In Viva Learning, we show the courses, which are part of an active library in SAP SuccessFactors. 

>[!Note]
> If the inputs are incorrect, MAC will generate error messages. To see the error messages, close the Viva Learning window in MAC and then reopen the window to refresh the validation.