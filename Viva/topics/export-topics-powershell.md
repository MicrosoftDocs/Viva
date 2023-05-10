---
ms.date: 05/10/2023
title: Export topics created in Viva Engage with PowerShell
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: ergradel
audience: admin
ms.topic: article
ms.collection:
  - m365initiative-viva-topics
  - Tier1
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
    - MET150  
ms.localizationpriority:  medium
description: Learn how to export topics created in Viva Engage (Lite Topics) to a .csv file.
---

# Export topics created in Viva Engage with PowerShell

Using PowerShell, you can export topics created in Viva Engage (also known as Lite Topics) to a .csv file. Topics created before enabling integration with Viva Engage are included.

> [!NOTE]
> This article assumes you have knowledge about how to use PowerShell.

## Requirements

To export the topics, you'll run a PowerShell script. Requirements to run the script are:

- PowerShell 7 or later. To install the latest version of PowerShell, go to [Installing PowerShell on Windows](/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3#installing-the-msi-package).
- The user running the script will need to be a Viva Topics admin or Knowledge Manager.

## Run the PowerShell script

1. [Get the script](#export-topics-script).
1. Use the following parameters: <br>
Export-TopicLite -Upn < string > | Export-Csv -Path < string >

Example:

```powershell
Export-TopicLite -Upn "user@domain.com" -Path "C:\"
```

## Output

The .csv file will include the following output:

- Display name
- Topic type
- Lifecycle status
- Time last modified

## Export topics script

```powershell
# Gets all topicLites
function Export-TopicLite()
{
    <#
    .SYNOPSIS
     Get all topic lites
    .DESCRIPTION

    .EXAMPLE
     Export-TopicLite -Upn "upn"
    #>
    [CmdletBinding()]
    param(
        [Parameter(Mandatory = $false)]
        [string] $Upn
    )

    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force
    $ErrorActionPreference = "Stop" 
    $VerbosePreference = "SilentlyContinue" 
    
    if ($PSVersionTable.PSVersion.Major -lt 7)
    {
        # You need to upgrade your PowerShell environment. REST and parallel execution has better implementation there.
        Write-Warning "PowerShell 7 or greater required.  REST and parallel execution has better implementation there."
        Write-Warning "If you are a part of Windows App Installer preview, use `"winget install --name PowerShell --exact`" from the command line to get and install the current stable version."
        Write-Warning "Otherwise go to `"https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows#installing-the-msi-package`" to download and install latest powershell"
        Write-Warning "See https://aka.ms/PSWindows for more"
        exit
    }

    . lib\AuthLib.ps1 
    . lib\TopicLib.ps1

    $SubstrateUri = "https://substrate.office.com"
    # Get default token to make call to Office Substrate Knowledge Base API
    $usertoken = GetUserToken -Portal:$SubstrateUri -upn:$Upn
    $token = ConvertTo-SecureString -string $usertoken -AsPlainText -Force

    # Breakdown token to get appropriate value for Substrate anchor for KM API calls
    $parsedToken = Parse-JWTtoken($token)

    
    $contentType = "application/json; charset=UTF-8"
    $headers = @{}
    $headers["Accept"] = $contentType
    $headers["Content-Type"] = $contentType

    # Required for correct routing of calls to Exchange Online
    $headers["X-AnchorMailbox"] = "SMTP:" + $parsedToken.upn
    $headers["X-RoutingParameter-SessionKey"] = "SMTP:" + $parsedToken.upn

    $data = $null
    # Need to assemble payload
    $topicUri = "$SubstrateUri/KnowledgeGraph/api/v1.0/Topics?provider=TopicLite"
    # Build body
    $headers["Client-Request-Id"] = [System.Guid]::NewGuid().ToString()
    $headers["X-Debug-FilterTopicLiteTopics"] = $false

    $lastName = ""
    $lastType = 1
    $lastId = "";
    $topicFound = $true
    $topics=[System.Collections.ArrayList]::new()

    while ($topicFound -eq $true)
    {
        try
        {
            if ($lastId -eq "")
            {
                $data = Invoke-RestMethod -Method GET -Uri $topicUri -Authentication Bearer -Token $token -Headers $headers
            }
            else
            {
                $nextTopicUri = $topicUri + "&lastId=$lastId&lastName=$lastName&lastType=$lastType"
                $data = Invoke-RestMethod -Method GET -Uri $nextTopicUri -Authentication Bearer -Token $token -Headers $headers
            }
        }
        catch
        {
            throw $_
        }

        if ($data.value.Length -ne 0)
        {
            $topics += $data.value
            $len = $data.value.Length
            $lastId = $data.value[$len-1].Id
        }
        else
        {
            $topicFound = $false
        }

        Write-Host "Last: $lastId Batch Len: $len"
    }
    return $topics
}

```
