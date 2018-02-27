---
# Metadata Sample
# required metadata

title: Using PS to assign users to AAD App
description: This describes how to use powershell to assign Workplace Analytics Roles in AAD for your Organization
author: rodonahu
ms.author: rodonahu
ms.date: 1/19/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Use Powershell to assign users to Azure Active Directory

## Install AzureAD PowerShell module

1. Open an elevated Windows PowerShell command prompt.
2. Run the following command -> ***Install-Module -Name AzureAD***. If prompted to install a NuGet module or the new Azure Active Directory V2 PowerShell module, type Y and press ENTER.
3. Run the following command to connect to your Office 365 subscription -> ***Connect-AzureAD***. In the Azure Active Directory PowerShell dialog box, type your Office 365 work account user name and password, and then click Sign in. Follow the instructions in the Azure Active Directory PowerShell dialog box to provide additional authentication information, such as a verification code, and then click Sign in.

## Identify the roles in Workplace Analytics

1. In the Azure Active Directory admin center, identify the &lt;Object ID&gt; that corresponds to the Workplace Analytics App<br>![Azure Active Directory admin center object id](../images/wpa/use/AADAdmin.png)
2. In the elevated Windows PowerShell command prompt that you opened above, run the following command -> $spo = Get-AzureADServicePrincipal -ObjectId &lt;Object ID&gt;.
3. Identify the roles by running the following command which will return all the available roles: -> $spo.AppRoles<br>![Workplace Analytics roles](../images/wpa/use/PS_1.png)
4. Get access to specific role.  You can see each role’s properties by checking the returned role.    
    - Program Manager:<br>***-> $programManagerRole = $spo.AppRoles | Where-Object {$_.DisplayName -eq 'Program Manager'}***<br>![Program manager role](../images/wpa/use/PS_2.png)
    - Administrator:<br>***-> $adminRole = $spo.AppRoles | Where-Object {$_.DisplayName -eq 'Administrator'}***<br>![Workplace Analytics administrator role](../images/wpa/use/PS_3.png)
    - Analyst Limited Access:<br>***-> $analystLimitedAccessRole = $spo.AppRoles | Where-Object {$_.DisplayName -eq 'Analyst (Limited Access)'}***<br>![Analyst limited access role](../images/wpa/use/PS_4.png)
    - Analyst<br>***-> $analystRole = $spo.AppRoles | Where-Object {$_.DisplayName -eq 'Analyst'}***<br>![Analyst role](../images/wpa/use/PS_5.png)

## Assign users to roles

1. In the Azure Active Directory admin center, identify the &lt;Object ID&gt; that corresponds to the user you want to assign to one of the roles<br>![Identify Object ID](../images/wpa/use/PS_6.png)
2. In the elevated Windows PowerShell command prompt that you opened above, run the following command -> ***$user = Get-AzureADUser -ObjectId &lt;objectid&gt;***
3. Run the following command -> ***New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $spo.ObjectId -Id &lt;$roleVariable&gt;.Id***, where ***$roleVariable***  should correspond to the corresponding role variable you want to assign the user to.<br>For example, if the user need to be assigned to Analyst role, then the command would be:<br>***-> New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $spo.ObjectId -Id  $analystRole.Id***

## Verifying user/s assignment to role/s

1. In the Azure Active Directory admin center, go to the Workplace Analytics App, you should see that **Total Users** equals the number of users you have assigned. <br>![Total Users](../images/wpa/use/AADADMIN_3.png)
2. Click on a user, then click **Applications**. You should see an entry that shows the role you have assigned to the user in the Workplace Analytics App.<br>![Verify roles](../images/wpa/use/AAD_ADMIN4.png)
