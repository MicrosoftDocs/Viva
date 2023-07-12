---
title: "Enforce Office 365 identity for Viva Engage users"
description: "When you enforce Office 365 identity in Viva Engage, all Viva Engage users use their Office 365 credentials to sign in to Viva Engage."
f1.keywords:
- CSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 06/28/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: 
- Adm_Yammer
- fwlink from UI
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 008f940b-6bec-47fc-bcc6-9c6133467562
---

# Enforce Office 365 identity for Viva Engage users

As Viva Engage becomes a core service for your organization, you'll want users to be able to log into it seamlessly, just like any other Office 365 service. Additionally, you'll probably want to maintain a single identity for all Office 365 users for easier user management. You can achieve both of these goals by enforcing Office 365 identity in Viva Engage. By enforcing Office 365 identity in Viva Engage and configuring password hash sync, pass-through authentication, or [Understanding Office 365 identity and Azure Active Directory](https://support.office.com/article/06a189e7-5ec6-4af2-94bf-a22ea225a7a9#BK_Federated) for Office 365, admins can achieve single sign-on (SSO) capabilities for all services in Office 365, including Viva Engage. 
  
## How enforcing Office 365 identities in Viva Engage works

The following flowchart shows what happens when a user logs in to Viva Engage.
  
:::image type="content" source="../../media/engage/admin/enforce-o365-id.png" alt-text="Flowchart shows what happens when user signs in when Office 365 identity is enforced, they log in with their Office 365 identity.":::
  
A user's sign-in experience when Office 365 identity is and isn't enforced for Viva Engage:
  
1. A user tries to log in to Viva Engage, and is presented with a sign-in dialog box.
    
2. The user enters their email address.
    
3. If Office 365 identity is enforced, the user will sign in with their Office 365 identity. If the customer has implemented the federated identity model in Office 365, the user signs in with single-sign-on.
    
4. If Office 365 identity isn't enforced, the user signs in with their Office 365 identity only if their email address corresponds to an Office 365 account.
    
5. When Office 365 identity isn't enforced, the user signs in with their Viva Engage identity (email and password), if their email address doesn't correspond to an Office 365 account.
    
The following table compares the user login behavior when Office 365 Identity is enforced or not enforced. Office 365 identity isn't enforced by default. 
  
| Is Office 365 identity enforced? | Is there an Office 365 account for that user's email address? | What happens when the user logs in: |
|:-----|:-----|:-----|
|Yes  <br/> |Yes  <br/> |The user is prompted to sign in with their Office 365 identity.  <br/> |
|No  <br/> |Yes  <br/> |The user is prompted to sign in with their Office 365 identity.  <br/> |
|No  <br/> |No  <br/> |The user is prompted to sign in with their Viva Engage identity (email and password).  <br/> |
   
<a name="StartEnforcing"> </a>
## Start enforcing Office 365 identity in Viva Engage

It takes just a few steps to start enforcing Office 365 identities in Viva Engage. However, turning on this setting can accidentally disrupt users' access to Viva Engage. So before you begin, do the following to make sure your Viva Engage users can continue working smoothly:
  
- **Make sure all current Viva Engage users have a corresponding Office 365 identity.** When you enforce Office 365 identities for Viva Engage, any user without a corresponding Office 365 identity is locked out of Viva Engage. So before you begin, make sure that all of your current Viva Engage users have corresponding Office 365 identities. To check this, go to the data export page within the Viva Engage admin center and export all users. Then compare that list to the list of users in Office 365 and make any needed changes. 
    
- **Tell your users about this change.** We strongly recommend that you tell users that you're switching to enforcing Office 365 identities, because it can disrupt their day-to-day usage of Viva Engage. See the following sample email for suggested text. 
    
You must be a global administrator on Office 365 who was synchronized to Viva Engage on Office 365.
  
### To start enforcing Office 365 identity in Viva Engage
  
1. In the Yammer admin center, go to the **Network Admin** section, and choose **Security Settings**.
    
2. In the Security Settings page, go to the **Office 365 Identity Enforcement** section and select **Enforce Office 365 identity**. 
    
    You must be a global administrator to see this section. 
    
    :::image type="content" source="../../media/engage/admin/enforce-o365-settings.png" alt-text="Screenshot that shows the Enforce Office 365 identity in Viva Engage checkbox in the Viva Engage Security Setting page. You must be a global administrator to see this setting.":::
  
3. A confirmation message asks you to select the most appropriate level of enforcement: 
    
   - **Committed Enforcement**:  Choose this option if all of your Viva Engage users already have an Azure Active Directory (AAD) account. 
    
     > [!IMPORTANT]
     > This change cannot be reversed. Your users will no longer be able to sign in using their Viva Engage usernames and passwords. 
  
   - **Temporary 7-Day Enforcement**: Choose this option if you're testing the enforcement of Office 365 identity on your network, and may need to revert it back. Once you save this change, a temporary enforcement period of seven days begins, and your users are no longer able to sign in using their Viva Engage usernames and passwords. After seven days, your network is automatically committed to Office 365 Identity enforcement.
    
     :::image type="content" source="../../media/a0927cc2-eafa-4ace-a939-a3fa27be943b.png" alt-text="Screenshot of confirmation dialog box that shows the Enforcement level for Office 365 sign-in.":::
  
4. If you want, you can automatically log out all current users, so that you can be sure that everyone using the Viva Engage service has logged in with their Office 365 identities. If you want to do log out all current users, select the **Log out all users** checkbox. If you choose to do this, we recommend that you communicate this change to your users by using the following sample email.
    
   *Subject Line: [Action Required] Log back in to Viva Engage* 
    
   *Hi,* 
    
   *This email is to let you know that [ORGANIZATION'S NAME] is making changes to the way we all access Viva Engage. If you're currently working on Viva Engage, then we may temporarily interrupt you by logging you out. It's necessary for us to securely setup Office 365 sign-in for Viva Engage.* 
    
   *You can resume your work immediately by logging in to Viva Engage using your Office 365 username and password.*
    
   *We've made this change so that you can access all of Office 365 with a single identity. If you're unable to log in using your Office 365 username and password, let your network administrator know.* 
    
   *Thank You,* 
    
   *[SIGNATURE]* 
    
5. If you're ready to start enforcing this setting, select **Okay**. Go to the Security Settings page where the **Enforce Office 365 identity in Viva Engage** checkbox is now selected. 
    
   > [!NOTE]
   > You can also select [Start blocking users who don't have Viva Engage licenses](../manage-viva engage-users/manage-viva engage-licenses-in-office-365.md#StartBlocking) to ensure that only users with Viva Engage licenses can login to Viva Engage. 
  
6. Choose **Save** to save all your settings on the page. 
    
   If you navigate away from this page, your settings won't take effect. 
    
## Stop enforcing Office 365 identity in Viva Engage
<a name="StopEnforcing"> </a>

> [!IMPORTANT]
> You can only stop enforcing Office 365 identities in Viva Engage when you are in the temporary 7-day enforcement period. 
  
When you stop enforcing Office 365 identities in Viva Engage:
  
- Any users already logging into Viva Engage with their Office 365 identities are unaffected by this change.
    
- Other users can join your network by signing up with their work email and verifying it.
    
If you no longer want to enforce Office 365 identities, you can follow the steps below to stop. You must be a global administrator to perform these steps.
  
**To stop enforcing Office 365 identity in Viva Engage**
  
1. In Viva Engage, go to the **Network Admin** section, and choose **Security Settings**.
    
2. In the Security Settings page, go to the **Office 365 Identity Enforcement** section and clear the **Enforce Office 365 identity** checkbox. 
    
   You see a confirmation message so you can verify that you're ready to stop enforcing Office 365 identity.
    
   :::image type="content" source="../../media/09162001-6581-41f9-b558-27673366c2a8.png" alt-text="Screenshot of confirmation dialog box to stop enforcing Office 365 identities in Viva Engage. Viva Engage SSO restarts if it was previously configured. Users who normally log into Viva Engage with Office 365 identities aren't affected.":::
  
3. Select **Okay** to confirm your choice. 
    
   This returns you to the Security Settings page where the **Enforce Office 365 identity in Yammer** checkbox is now cleared. 
    
4. Choose **Save** to save all your settings on the page. 
    
   If you don't choose **Save** but instead navigate away from the page, your settings won't take effect. 
    
## FAQ
<a name="FAQ"> </a>

### Q: Once Office 365 Identity Enforcement is set to 'Committed Enforcement', why can't I revert it back?

A: Once your organization has committed to enforcing Office 365 identity and has one Office 365 tenant associated with a single Viva Engage tenant, connected groups are enabled for this network.. In this configuration, whenever a group is created in Viva Engage, a connected Microsoft 365 group is also created, and users can take advantage of tools like SharePoint, Planner, and OneNote connected to the group. At this point, reverting the **Enforce Office 365 Identity** setting will be disruptive to the user experience, since users who sign in with their user names and passwords can't access these connected resources any more.
  
### Q: How will this change impact guest and external users?

A: Guests and external users are unaffected and will follow the sign-in settings and requirements of their home network. 
  
### Q: How long does it take for this setting to be applied?

A: Enforce Office 365 Identity is applied immediately after the setting is set.
  
### Q: We use the same ADFS configuration in Viva Engage and Office 365. Should we sign out users during the transition?

A: Yes. Sign-out ensures all users who sign on afterward are connected to their Office 365 identity. Office 365 identity connects users to lifecycle management from Office 365. It also provides a consistent experience for them, with things like Office 365 suite navigation.
  
### Q: What is the experience for users being logged-out when enforcing Office 365 identities?

A: Users will be signed out of their web and mobile sessions immediately and must sign in again to all their devices and browser sessions using their Office 365 identity configuration and credentials.
  
### Q: How can I audit and clean up Viva Engage users when compared to Office 365 and Azure AD?

A: You can audit Viva Engage users in networks connected to Office 365 and take appropriate actions based on it. See more information and examples in [How to audit Viva Engage users in networks connected to Office 365](../manage-viva-engage-users/audit-users-connected-to-office-365.md).
