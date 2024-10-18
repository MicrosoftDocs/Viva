---
title: "Improve Microsoft 365 sign-in for Viva Engage with auto-acceleration policy"
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
ms.custom:
- Adm_O365
- Adm_Yammer
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
ms.assetid: 4d0e5067-992c-4cd6-bad5-b4ac0d52f596
description: "Create an auto-acceleration policy to improve Microsoft 365 sign-in for Viva Engage."
---

# Improve Microsoft 365 sign-in for Viva Engage with auto-acceleration policy

To improve the Microsoft 365 sign-in experience for Viva Engage, use the Auto-acceleration policy to accelerate directly to the ADFS federated domain, bypassing the Office 365 sign-in page. 
  
## Prerequisites

- You must be a Microsoft 365 Global Administrator to run the PowerShell commands.
    
- Download and install the [Azure Active Directory v2 PowerShell Module](https://www.powershellgallery.com/packages/AzureAD/2.0.2.16).
    
- Open administrative Azure AD PowerShell and run following commands:

     > [!IMPORTANT]
     > The `Save-Module` command downloads the module from the Internet. You need a working internet connection on the computer where you run these commands. 
    
    ```powershell
    Save-Module -Name AzureAD -Path <path>
    ```

   

  
    ```powershell
    Install-Module -Name AzureAD
    ```

## Enable policy

1. Run the following commands:
    
    Connect to Tenant's Microsoft Entra ID. This command prompts you to sign in using admin credentials.
    
      ```powershell
     connect-AzureAD [-tenantID | -tenantDomain] <tenant name>
     ```

    :::image type="content" source="../../media/7f7c2ac7-b7dc-4ee1-b5c6-32b3c2ae6dc1.jpg" alt-text="Screenshot showing an example sign-in using admin credentials.":::
  
2. Check that no policy of the same name already exists.
    
      ```powershell
      get-AzureADPolicy
      ```

3. Create a new policy:
    
  - If you have a single federated domain that authenticates users for applications, set human resource development (HRD) policy by running the following command:
    
     ```powershell
      New-AzureADPolicy -Definition @("{`"HomeRealmDiscoveryPolicy`":        {`"AccelerateToFederatedDomain`":true}}") -DisplayName
       BasicAutoAccelerationPolicy -Type HomeRealmDiscoveryPolicy
    ```

    If you have multiple federated domains and have a preferred domain for your application against which users authenticate, set Policy by typing the following command:
    
       ```powershell
     ` New-AzureADPolicy -Definition @("{`"HomeRealmDiscoveryPolicy`":{`"AccelerateToFederatedDomain`":true,`"PreferredDomain`":`"contoso.com`"}}")
    -    Displ`ayName BasicAutoAccelerationPolicy -Type HomeRealmDiscoveryPolicy
       ```

4. Note the object-id of the policy you created:
    ```powershell
    get-AzureADPolicy
    ```
    :::image type="content" source="../../media/622b3fcc-ed8b-4941-85be-e045b153607e.jpg" alt-text="Screenshot showing an example output of new policy.":::

5. Note the **ObjectId** of servicePrincipal for Viva Engage application (Redirect output to a text file for easy search). The AppDisplayName would be "Office 365 Viva Engage" with AppID of 00000005-00000ff1-ce00-000000000000 
    
    ```powershell
    Get-AzureADServicePrincipal -All $true | fl > output.txt
    ```
    :::image type="content" source="../../media/31fee97b-75a2-498e-b404-c925f018615f.jpg" alt-text="Screenshot of Command line for redirecting output to a text file.":::

    :::image type="content" source="../../media/063f131c-413a-4372-8b11-e79a41e421b2.jpg" alt-text="Screenshot of an example of output to a text file.":::
  
6. Finally, add the policy for Viva Engage service:
    
      ```
      Add-AzureADServicePrincipalPolicy -ID <ObjectID of the Service Principal copied from #5> -RefObjectId <ObjectId of the Policy copied from #4>
      ```

    :::image type="content" source="../../media/3547246b-9d0f-4f97-9910-14c9559bf2fa.jpg" alt-text="Screenshot of Command line for adding the policy for Viva Engage service.":::
  
## List of commands in order

To enable the policy, you must run the following commands. Run them one line at a time and review the output after each command:
  
```Powershell
Connect-AzureAD -TenantDomain <Tenant-Name>
get-AzureADPolicy
$PolicyId = New-AzureADPolicy -Definition
@("{`"HomeRealmDiscoveryPolicy`":{`"AccelerateToFederatedDomain`"
:true}}") -DisplayName BasicAutoAccelerationPolicyforViva Engage -Type HomeRealmDiscoveryPolicy
get-AzureADPolicy
$yamObjectId = Get-AzureADServicePrincipal -All $true | ?{$_.AppDisplayName -eq 'Office 365 Viva Engage'}
Add-AzureADServicePrincipalPolicy -Id $yamObjectId.ObjectId - RefObjectId $PolicyId.Id
```

Note: If you have multiple federated domains, adjust the third command appropriately.
  
## Testing

In a new in-private browser session, sign in to Viva Engage with user credentials from the federated domain. Your sign-in workflow should skip the Microsoft Entra ID page and go straight to the ADFS sign-in page.  
  
## Scenarios

The following table summarizes the authorization flows for this policy.
  
|**Login**|**Flow without policy**|**Flow with policy**|
|:-----|:-----|:-----|
|Viva Engage.com  <br/> |Email address \> Microsoft Entra sign-in \> ADFS sign-in  <br/> |Email address \> ADFS sign-in  <br/> |
|Viva Engage.com/mycompany.com  <br/> |Email address \> Microsoft Entra sign-in \> ADFS sign-in  <br/> |Email address \> ADFS sign-in  <br/> |
