---
title: "Manage Viva Engage users across their lifecycle from Microsoft 365"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/24/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 6c4c8fff-6444-404a-bffc-f9da0bcc3039
description: "Manage Viva Engage Enterprise users in Microsoft 365. As you create, delete, and restore users in Microsoft 365, they're created, deactivated, and reactivated in Viva Engage."
---

# Manage Viva Engage users across their lifecycle from Microsoft 365

There are many types of users in Viva Engage and managing each of them is different.

- Users with a Microsoft Entra ID
- Users without a Microsoft Entra ID
- Guests

As a Microsoft 365 Global Administrator, you control the lifecycle for Viva Engage users through the Microsoft 365 admin center, in addition to managing them through Viva Engage.

All communities and groups from Viva Engage networks in Native Mode are managed through these admin centers. Some of the management capabilities regarding community or group members or users that can be done through the Microsoft 365 admin center includes:

- Add or remove community or group members
- Manage community or group ownership
- Delete a community or group
- Restore a community or deleted group
- Rename the community or group
- Update the community or group description
- Change the community's or group's privacy setting

When you create users in Microsoft 365, they can sign in to Viva Engage with their Microsoft 365 credentials. When a user is deleted from Microsoft 365, they're automatically deactivated or suspended in Viva Engage. When a user is restored in Microsoft 365, they're reactivated in Viva Engage.
  
The user's profile properties (such as name and department) from Microsoft Entra ID are automatically populated in the user's Viva Engage profile. Any changes to the profile properties in Microsoft Entra ID are reflected in Viva Engage.

If users have a Microsoft 365 account, they can't update their information directly in Viva Engage. If users want to change their information, such as photos, phone numbers, and other data, they must update it through their Microsoft 365 profile just as they would with other Microsoft 365 apps. If the organization permits it, users can update through Microsoft Delve. A user might need to ask their IT administrator to assist.

> [!Important]
> If a user had a customized profile prior to April 2020, it will be overwritten with their Microsoft Entra identity to create a single source of truth.

When a user's Viva Engage account is activated, Viva Engage takes the language setting in Microsoft 365. If the user or admin changes their language setting in Microsoft 365 or Microsoft Entra ID, Viva Engage doesn't pick up this change. The user can change their Viva Engage language setting in their Viva Engage profile on the **Preferences** tab.

This change means that we retire properties that aren’t synced today, like a user’s personal email account information. If you’d like to maintain information data from the **About Me** settings – such as Schools, Expertise, and Interest - we recommend that you export this data. Use Microsoft Graph to update the users’ Microsoft 365 profile, or ask users to update it themselves in Microsoft Delve.

## How are user photos managed?

If new users in your network already have the correct user photo from Microsoft Entra ID, it continues to work after this change.

If your organization usually uploads photos from Viva Engage, you can follow these steps:

1. Export the list of users.
2. Use that list of users to export their photos via a script.
3. Upload them with Microsoft Graph to add the photo to the rest of Microsoft 365.
  
## Create a user

The user creation process varies depending on when the Viva Engage network was created.

### Networks created before March 2019

Beginning in March 2019, we changed how Viva Engage users are created. The process differs for existing Microsoft 365 users versus new Microsoft 365 users.

- **Pre-March 2019**: Viva Engage users are created when they use Viva Engage for the first time.

    The process of creating a user requires these steps:
  
    1. The Microsoft 365 Global administrator creates a user in Microsoft 365.
    
    2. The user signs in to Microsoft 365 using the identity provider configured for the tenant.
    
    3. The user selects the Viva Engage tile in the Microsoft 365 app launcher to go to Viva Engage.
    
    4. A new Viva Engage user is created for the Microsoft 365 user. The user's profile properties and language setting from Microsoft Entra ID are automatically populated in the user's Viva Engage profile.

### New networks, Native Networks, and Enforced Microsoft 365 Identity Networks 

When **Enforce Office 365 identity** is selected in Viva Engage (including when in Native Mode), as Viva Engage-eligible users are added to Microsoft 365, they're automatically added as pending users in Viva Engage. Their status changes from **Pending** to **Active** the first time they use Viva Engage.

The process follows these steps:
  
1. The Microsoft 365 Global administrator creates a user in Microsoft 365.
    
2. A pending user is created in Microsoft 365. The first time the user uses Viva Engage, the pending user becomes an active user.

- **During transition**: Different actions are taken for different user categories:

    |**Type of user**|**Viva Engage network configuration**|**Way that they are added**| 
    |:-----|:-----|:-----|
    |New users added to your Microsoft 365 tenant|**Enforce Office 365 identity** selected|Users are automatically added as pending users in Viva Engage. 
    | Existing users in your Microsoft 365 tenant|**Enforce Office 365 identity** selected|Microsoft 365 users must use Viva Engage to be added as a Viva Engage user. |

    
## Block a user

When a Microsoft 365 Global administrator blocks a user in Microsoft 365, the user is signed out of Viva Engage and all other Microsoft 365 services.

The process follows these steps:
    
1. In the Microsoft 365 admin center, select a user and choose **Edit User**. The **Sign-in status** appears in the user details.
  
2. Select **Edit** next to **Sign-in status** and switch **Allow the user to sign in** to **Block the user from signing in**.
  
This action flows into Viva Engage, and the corresponding user is signed out of Viva Engage (on all devices). The next time this user tries to sign in to Viva Engage from any device, they're prompted to sign in with their Microsoft 365 credentials. However, the user can't sign in because their sign-in status is set to blocked. As a Viva Engage verified administrator, you can look at the Account activity in the Network Admin area to verify that the Viva Engage user is signed out (that is, they have no active Viva Engage sessions).
    
 :::image type="content" source="../../media/c0704de5-d3c4-4b34-9bbb-f3cf31799734.png" alt-text="Screenshot of the Account Activity for a user showing no active Viva Engage sessions (logged out).":::
  
## Delete a user

If an employee leaves the company, you can delete the user from Microsoft 365. When the user is deleted from Microsoft 365, the corresponding user is deactivated (also known as suspended) in Viva Engage. The following diagram shows how this works:
  
The process follows these steps:
  
1. An admin deletes a user from Microsoft 365.
  
2. The user deletion in Microsoft 365 flows into Viva Engage, and the corresponding Viva Engage user is deactivated in Viva Engage. You can do the same operation in Viva Engage admin center: choose **Remove Users** and select **Deactivate this user**.

    :::image type="content" source="../../media/91299919-212c-41f9-b6dd-185c0b81de65.png" alt-text="Screenshot showing how to deactivate a user in Viva Engage.":::
  
    Deactivated (or suspended) users show up in Viva Engage administration pages as being deactivated by **System Administrator**, as shown in the following screenshot: 
    
   :::image type="content" source="../../media/b0ac3142-1fba-4c52-95d8-bbbb063cdaa2.png" alt-text=" Screenshot that shows a user removed by System Administrator.":::
  
    When you delete a user in Microsoft 365, the user becomes inactive. After approximately 30 days, user data gets permanently deleted. See [Delete a user from your organization](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
    
    Similarly, when a user is deactivated in Viva Engage, that user becomes inactive in Viva Engage. After approximately 90 days, deactivated users are permanently removed, but their name, files, messages and activity data are retained. 
    
 > [!IMPORTANT]
 > When you delete a user from Microsoft 365 and this flows through to Viva Engage, the user's name, files, messages, and activity data remain in Viva Engage even though the user is deleted. For options that remove a user in a way that the user's name and data are also deleted from Viva Engage, see [Remove users](add-block-or-remove-users.md#RemoveUsers) and [Manage GDPR data subject requests in Viva Engage Enterprise](../manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md). 
  
## Restore a user

When an administrator restores a Viva Engage-eligible user in Microsoft 365, the user is reactivated in Viva Engage. The following diagram shows how this works:
  
The process follows these steps:
  
1. The Microsoft 365 administrator can restore a deleted user in Microsoft 365, as shown in the following screenshot:
    
    :::image type="content" source="../../media/b30aa7c8-2e2d-45ed-9c0a-2bf9730c8b30.png" alt-text="Screenshot showing the command to restore a user in Microsoft 365 administration.":::
  
2. This action flows into Viva Engage as well, and the previously deactivated user in Viva Engage is reactivated.
    
## User profile information

The user profile experience differs depending on whether or not the account is connected to Microsoft Entra ID.

<a name='for-azure-ad-connected-accounts'></a>

### For Microsoft Entra connected accounts

Microsoft 365 uses the cloud-based service Microsoft Entra ID to manage users. In an on-premises environment, you can manage users in the cloud, or create and synchronize users, communities, or groups in [Microsoft 365  and Microsoft Entra ID](https://support.office.com/article/06a189e7-5ec6-4af2-94bf-a22ea225a7a9). 

When Microsoft 365 users who are new to Viva Engage access Viva Engage for the first time using their Microsoft Entra credentials, a Viva Engage user is created. The Viva Engage user profile is then populated with the Microsoft Entra user properties. When the user's profile properties are edited in Microsoft Entra ID, they're updated in the existing user's Viva Engage profile. For example, if the user's department changes in Microsoft Entra ID, it also changes in Viva Engage.
  
User profiles that they see in Viva Engage are their Microsoft 365 profile, if their organization uses Microsoft Entra ID to manage user credentials.
  
- To view their profile in Microsoft 365, users can select on their profile picture and choose **My account**.
    
   :::image type="content" source="../../media/yammer-identity-user-profile.png" alt-text=" Screenshot of the Microsoft 365 profile picture.":::
  
    **My account** displays a user's account information for Microsoft 365. If the organization allows editing personal information, then users can select **Personal Info**, and add the information they want. If the organization doesn’t allow editing, then the settings won't be editable and users see a **Why can’t I edit** link they can select for more information.

    User photos are synced from Microsoft. To prepare for this change, make sure your organization’s photos can be found in any one of the following places:

    - Go to the All users list in the Microsoft Entra admin center and then select the desired user for picture.
    - Confirm the My account page in the Microsoft portal has the photo.
    - Get the Photo API using the Microsoft Graph preview.
    - Get-the UserPhoto Exchange Online cmdlet, if applicable.

    
- To view their profile in Viva Engage, users can choose **Edit Settings**, and then **Profile**.
    
  
### For non-Azure AD accounts

If your Viva Engage users aren't in Microsoft Entra ID, then they can update their profiles in Viva Engage by clicking Edit Settings, and then Profile.
  
:::image type="content" source="../../media/e9378a05-bb94-4775-9336-818333e65edf.png" alt-text="Screenshot showing a sample user profile.":::
  
The Microsoft 365 Global administrator can edit user properties from the Microsoft 365 admin center.
  
 **To edit user properties in Microsoft 365**
  
1. In the Microsoft 365 admin center, go to the **Users** section, and select or search for a user, as shown in the following screenshot. 

   :::image type="content" source="../../media/b045e652-c971-46c2-a37a-a2d2cc872838.jpg" alt-text="Screenshot showing the Users section of Microsoft 365 admin center.":::
  
2. Select on the user, and choose **Edit** to change the properties, such as Username or Contact information. 
    
   :::image type="content" source="../../media/57657206-20e3-4c1e-811a-dd6b0df1beaa.jpg" alt-text="Screenshot showing editing profile properties.":::
  
   Microsoft Entra ID updates the following Viva Engage properties:
  
   | Property in Microsoft Entra ID | Property in Viva Engage |
   |:-----|:-----|
   | Email address  <br/>  Display Name  <br/>  Job Title  <br/>  Department  <br/>  Office  <br/>  Office phone  <br/>  Mobile phone  <br/>  Description  <br/> | Email  <br/>  Display Name  <br/>  Job Title  <br/>  Department  <br/>  Location  <br/>  Work phone  <br/>  Mobile phone  <br/>  About Me  <br/> |
   
   In Microsoft 365, you can see the user properties that are updated for Viva Engage in the following dialog boxes:
  
   - **Edit email addresses** dialog box 
     - **Edit contact information** dialog box 
    
       :::image type="content" source="../../media/78cb9ff3-a1a3-4bff-be12-e584c36063f8.jpg" alt-text="Screenshot showing editing contact information.":::
  
  
## FAQ

#### Are user profile pictures updated from Microsoft 365 to Viva Engage?

Yes. The profile is updated with the user's Microsoft 365 profile picture. This update is initiated when the user selects the Viva Engage tile from Microsoft 365 or logs in to Viva Engage. Changes are reflected in the Viva Engage profile within a few hours. If the user later updates his or her profile picture, the Viva Engage profile picture updates after the user next uses Viva Engage.
  
#### When an email address is changed in Microsoft 365, does it trigger an email address change in Viva Engage?

Yes.
  
#### What happens when a user leaves the company?

When a user leaves the company and Microsoft Entra ID is updated, their Viva Engage profile content is replaced with their start and end dates, and their title is changed to **Former member**. All the messages and files they posted remain in Viva Engage. 

   :::image type="content" source="../../media/yam_former_member.png" alt-text="Screenshot showing Viva Engage profile content.":::

#### My company has a configuration where not all Viva Engage users are yet in Microsoft 365. How does life cycle management work in this case?

The users who sign in Viva Engage with Microsoft 365 credentials can be managed in Microsoft 365. You can continue to manage the users who don't use their Microsoft 365 credentials the same way you manage them today. Eventually, when you move everyone to Microsoft 365, you'll have one single place to manage all your users.
  
## Related articles

[Manage a Viva Engage community or group](https://support.office.com/article/12ce0216-0618-4576-b87a-a8c189cee0f8)

[Change my profile settings](https://support.office.com/article/cb9b9f8b-391d-424b-b752-5e23619fadec)

[Add, block, or remove Viva Engage users](../manage-viva-engage-users/add-block-or-remove-users.md)
