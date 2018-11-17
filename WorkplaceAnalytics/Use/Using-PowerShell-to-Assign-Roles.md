---
# Metadata Sample
# required metadata

title: Assign roles with PowerShell in Azure Active Directory
description: How to use PowerShell to assign Workplace Analytics roles in Azure Active Directory.
author: rodonahu
ms.author: madehmer
ms.date: 11/16/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Assign Workplace Analytics roles with PowerShell in Azure Active Directory

## Install AzureAD PowerShell module

1. Open an elevated Windows PowerShell command prompt.
2. Run the following command: **Install-Module -Name AzureAD**
3. If prompted to install a NuGet module or the new Azure Active Directory v2 PowerShell module, type **Y** and then press **ENTER**.
4. Run the following command to connect to your Office 365 subscription: **Connect-AzureAD**
5. In the Azure Active Directory PowerShell dialog box, type your Office 365 work account user name and password, and then select **Sign in**.
6. If prompted, follow the instructions for additional authentication information, such as a verification code, and then select **Sign in**.

## Identify the roles in Workplace Analytics

1. In the Azure Active Directory admin center, identify the &lt;Object ID&gt; that corresponds to the Workplace Analytics App.

    ![Azure Active Directory admin center object id](../images/wpa/use/AADAdmin.png)

2. In the elevated Windows PowerShell command prompt that you opened above, run the following command: **&#36;spo = Get-AzureADServicePrincipal -ObjectId &lt;Object ID&gt;**

3. Identify the roles by running the following command, which will return all the available roles: **&#36;spo.AppRoles

    ![Workplace Analytics roles](../images/wpa/use/PS_1.png)

4. Get access to specific roles.  You can see each role’s properties by checking the returned role.

    - **Program Manager**: &#36;programManagerRole = &#36;spo.AppRoles | Where-Object {&#36;_.DisplayName -eq 'Program Manager'}

      ![Program manager role](../images/wpa/use/PS_2.png)

    - **Administrator**: &#36;adminRole = &#36;spo.AppRoles | Where-Object {&#36;_.DisplayName -eq 'Administrator'}

      ![Workplace Analytics administrator role](../images/wpa/use/PS_3.png)
    - **Analyst Limited Access**: &#36;analystLimitedAccessRole = &#36;spo.AppRoles | Where-Object {&#36;_.DisplayName -eq 'Analyst (Limited Access)'}

      ![Analyst limited access role](../images/wpa/use/PS_4.png)
    - **Analyst**: &#36;analystRole = &#36;spo.AppRoles | Where-Object {&#36;_.DisplayName -eq 'Analyst'}

      ![Analyst role](../images/wpa/use/PS_5.png)

## Assign users to roles

1. In the Azure Active Directory admin center, identify the &lt;Object ID&gt; that corresponds to the user you want to assign to one of the roles.

    ![Identify Object ID](../images/wpa/use/PS_6.png)

2. In the elevated Windows PowerShell command prompt, run the following command: **$user = Get-AzureADUser -ObjectId &lt;objectid&gt;**
4. Run the following command, where **&#36;roleVariable** corresponds to the role variable you want to assign the user to:
     **New-AzureADUserAppRoleAssignment -ObjectId &#36;user.ObjectId -PrincipalId &#36;user.ObjectId -ResourceId &#36;spo.ObjectId -Id &lt;&#36;roleVariable&gt;.Id**

   For example, to assign a user the Analyst role, you'd run this command:
     **New-AzureADUserAppRoleAssignment -ObjectId &#36;user.ObjectId -PrincipalId &#36;user.ObjectId -ResourceId &#36;spo.ObjectId -Id &#36;analystRole.Id**

## Verifying user assignments to roles

1. In the Azure Active Directory admin center, go to the Workplace Analytics App, you should see that **Total Users** equals the number of users you have assigned. 

   ![Total Users](../images/wpa/use/AADADMIN_3.png)

2. Select a user, and then select **Applications**. You should see the role you have assigned to the user for the Workplace Analytics App.
   ![Verify roles](../images/wpa/use/AAD_ADMIN4.png)
