---
title: "Configure your Viva Engage network"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 07/26/2023
audience: Admin
ms.topic: article
ms.localizationpriority: medium
ms.custom: Adm_Yammer
ms.service: viva
ms.subservice: viva-engage
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: f886e916-fe64-41de-be52-38d458250fa5
description: "Use the Viva Engage admin tools to set up your Viva Engage network. Covers options for configuration, design, admins, usage policy, external networks, and activity stream keys."
---

# Configure your Viva Engage tenant

To ensure that your users have a consistent experience, complete these tenant configuration tasks in the Viva Engage admin center before inviting users to Viva Engage Enterprise.
  
As you get started with Viva Engage, review the links in [Viva Engage admin help](../eac-overview.md) for other tasks you might want to do, such as [reviewing security and compliance settings](../manage-security-and-compliance/security-and-compliance.md).
  
To access the Viva Engage tenant settings:
  
- In Viva Engage, select the settings icon and go to Admin center.
- In the admin center, on the **Setup and configuration** tab, select **Tenant settings**.

#### Set the tenant name

> [!IMPORTANT]
> In Microsoft 365 or Office 365 Viva Engage tenants, the name in the Microsoft 365 or Office 365 company profile overrides the tenant name setting in Viva Engage. To change the company profile settings, see [Change your organization's address, technical contact, and more](/microsoft-365/admin/manage/change-address-contact-and-more)
- From the **Tenant settings** page, set the tenant name.

#### Set a usage policy 
To ensure that content is office‐appropriate, you may want to create a usage policy for engagement. For instructions and best practices, see [set up a usage policy](../set-up-usage-policy.md).

#### Upload a Tenant logo
As a Engage admin, network admin, or verified admin, you can choose to upload the org’s logo on the Viva Engage tenant. This logo appears on the user’s home feed and leadership corner header. 
- Use the **Tenant logo** setting to add an image. Only one image can be uploaded at a time.

#### Choose a language for system messages
System messages notify users of important actions in the network and conversations, such as creating a new group or adding people to a conversation.  
 - From the **Language** setting, choose a language for system messages. 
 All future system messages appear in the language you choose. Existing system messages appear in the previous language.

#### Require users to confirm email messages before posting
- From the **Configuration** page, in the **Email Settings**, select whether to require users to confirm messages posted using email before posting.
For more information about email and Viva Engage, see [Configure email and Viva Engage](configure-email-and-viva-engage.md).

#### Restrict who can upload files and limit file formats
1. On the **Configuration** page, in the **File Upload Permissions** section, set which types of files can be uploaded.

2. To allow unlimited file types, select **Allow people to upload and attach files in any format**.

    Any number of files, images, or both can be attached to any message or reply, with each file size limited to 5 GB. By default, file attachments are enabled.

 > [!NOTE]
 > Uploading an image wider than 7680 pixels or taller than 4320 pixels will result in an error.
  
3. To restrict who can upload files, clear the **Allow people to upload and attach files in any format** checkbox. 
Choose from these three options:

      - **Allow people to upload and attach files in any format**

      - **Only allow people to upload and attach image or video files**: Limits attachments to images and videos. Viva Engage determines file type by extension.

         Viva Engage uses Azure Media Services to make videos viewable within the network. For more information, see [Azure Media Services](https://azure.microsoft.com/products/media-services/).

      - **Don't allow anyone to upload or attach files**: When selected, this option prevents people from uploading and attaching new files. Eexisting attachments aren't affected.

> [!NOTE]
> When files are stored in Viva Engage, there is no virus check. An admin can export the files and perform an offline virus scan on them, and this process can be automated with custom scripting.
>
> For Microsoft 365 connected Viva Engage groups that store files in SharePoint, virus checking is done as the file is uploaded. For more information, see [Virus dectection in SharePoint Online](/office365/securitycompliance/virus-detection-in-spo).

> [!TIP]
> Any admin can delete any file, and group admins can delete files posted to the groups that they manage.
>
> To delete files, a network admin can click the Viva Engage **Settings** icon and then click **Files**. This brings up the **Files** directory for the entire network. Group admins can delete files posted to a group by going to the **Files** tab within the group they administer.
  
#### Enable or restrict the use of third-party apps

The growing network of partners and developers in Viva Engage continue to build third-party applications using an API. To find the list of current apps, go to the [App Directory](https://go.microsoft.com/fwlink/?LinkId=524143). There, you can find integrations with Microsoft SharePoint, Microsoft Flow, Microsoft Dynamics, and many other business applications.
  
- On the **Configuration** page, in the **Enabled Features** section, specify whether to allow third-party applications.

 > [!CAUTION]
 > Clearing this setting prevents users from adding or accessing these applications. Note that all users, including verified admins, will lose access to apps that were added prior to clearing this setting.

 > [!NOTE]
 > This setting does not apply to Microsoft 365 or Office 365 connectors that can be added to Microsoft 365 groups. To disable use of these connectors in Viva Engage, use the following PowerShell command:  
 >```Set-OrganizationConfig -ConnectorsEnabledforYammer:$false```
 > 
 > For more information, see [Manage Microsoft 365 Groups with PowerShell](/office365/enterprise/powershell/manage-office-365-groups-with-powershell).

#### Allow Tenor GIFs in messages

By default, users can attach GIFs provided by Tenor, a third-party company, to posts.

> [!NOTE]
> The GIF search in Viva Engage defaults to Tenor's "young audience" and "strict" filters to keep GIFs appropriate in a school or work setting. If you see inappropriate GIFs in a search, send email to support@tenor.com with a link to the GIF.

You can turn off this feature so that users don't see GIFs from Tenor.

- From the **Configuration** page, in the **Enabled Features** section, turn off **Show Tenor GIFs Search**.

#### Control how links are displayed

By default, when creating a message with a URL, Viva Engage fetches content associated with third-party websites, including title, summary, images, and GIFs. Existing URLs that are cached remain until the cache expires.

You can turn off the display of this data for links.

- On the **Configuration** page, in the **Enabled Features** section, enable or disable **Fetch URL Content**.

#### Allow users to view an org chart in Viva Engage

The org chart was retired for Office 365 Viva Engage networks in May 2018. Office charts are available at Skype for Business and Delve. For more information, see [Find info from a contact card in Skype for Business](https://support.office.com/en-us/article/Find-info-from-a-contact-card-in-Skype-for-Business-d797905c-66f0-4248-b473-c49e3c9a0767) and [How can I find people and information in Office Delve?](https://support.office.com/en-us/article/How-can-I-find-people-and-information-in-Office-Delve-5b8bffdd-a50a-430a-8570-09b39481887c)
  
#### Allow message translation

This feature gives users the option to translate messages from [any language supported by Microsoft Translator](https://www.microsoft.com/en-us/translator/languages.aspx) into the network's default language. To enable this feature, the network admin must accept a Terms and Services agreement in order to use Microsoft's proprietary translation technology. This feature is disabled by default.

When this enabled, users have a **Translate** option with any message posted in a language different than the language they've selected in **Preferences** in their Viva Engage settings.
  
- On the **Configuration** page, in the **Enabled Features** section, select whether to allow **Message Translation**.

