---
title: Viva Goals - Jira On-Prem Troubleshooting Tips
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Setting up your Viva Goals integration with Jira hosted on premise with trouble shooting tips."
---

# Viva Goals - Jira On-Prem Troubleshooting Tips

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Troubleshooting guidelines for issues in the Viva Goals - Jira (application link) integration

If your Jira instance is hosted on-premise (self-managed), here are a couple of troubleshooting guidelines to refer to while setting up the integration. If you're yet to set up the Viva Goals - Jira (On-Premise) integration, then head on over to this [help article.](https://help.ally.io/en/articles/2285939-jira-integration)

Watch this video to see how the Jira  Application Link setup looks like!


#### 1. While creating a Jira connection, I'm seeing  the error message: 'Unauthorized'

There are 2 reasons why this could be happening,

- Check if you've selected the right Jira instance type for the question **How is this Jira instance hosted?** in the new connection screen. If you have a Jira cloud-hosted instance, select **Cloud**. If you have your own on-premise instance, select **Jira-Server**.  

    :::image type="content" source="../media/goals/goals-creating-jira-connection.png" alt-text="Image of Jira connection":::

- Check if the following setup data has been provided correctly in your Jira application link configuration in your Jira instance. 
    
    1. Is your config application link https://app.ally.io? 
    
    1. Have you enabled the **Create incoming link** option? 
    
    1. Are the Consumer Key and Public Key provided correctly? Copy the consumer key and public key given below: 
    
        Consumer key:JZbA9Qo_eodgQvPj8Tex
        
        Public key:
        
        -----BEGIN PUBLIC KEY-----
        
        MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCRrvXSpKjISLHC8ghilMI3aQ0qvZeTk2sBYOy/2MXQ6nqYCDIq6ukAay0ZWGNmhlFz4vJ6LKIt02V3ufgB26pgwSa9gR0PJ4oYQoTQMOBBOfXZcvXJCDL9C6DGbNehXCfxDvGXf867dxaVuPeeCca8vUhPDSBaUxsL+f8KifCCfQIDAQAB
        
        -----END PUBLIC KEY-----

    > [!NOTE]
    > You can verify the steps in this [help article](https://help.ally.io/en/articles/2997829-jira-integration-setting-up-an-application-link) to check if the application link has been set up correctly.

#### 2. While creating a Jira connection, I'm seeing the error message: “Service Unavailable”

Here are a few settings to check: 

- **Is the Jira server URL provided valid and accessible?**  

    Check if the Jira server URL you've provided follows this format: http://myjirapp.com/ and is reachable on HTTPS port.  

- **Is your Jira server URL behind a firewall?**

    If your Jira server URL is behind a firewall, you'll have to add the following IPs to the allowlist:
 
    54.243.192.208 <p>
    3.225.237.0 <p>
    107.20.38.17 <p>
    23.21.1.160

#### 3. While creating a Jira connection, I'm seeing  the error message: “Please re-check your Jira credentials” or “Invalid credentials”

- **Check your Jira Credentials**: Check if the Jira server is accessible using the credentials which were used when connecting with Viva Goals. 

- **Check the option selected on the consent screen on Sign-in**: After the user select “Sign in with Jira”, the user will land on a window showing the consent screen, and the user can either select Allow or Deny or close the popup. 

- **Allow**: Clicking this will create the connection successfully. 

- **Deny**: Clicking this will throw the error: Invalid credentials. Closing the popup is similar to denying. 

#### 4. While creating a Jira connection, I'm seeing  the error message: “Invalid server URL”

- Check if the Jira server URL provided is a valid one, is it syntactically right? 

- Also check if you're able to access the Jira server directly or from other sources, apart from Viva Goals.

#### 5. After clicking on sign-in, either the pop-up window keeps loading or you get a different error (maybe something like an application error). 

This would likely be an issue where Viva Goals isn't able to establish a connection with the Jira server, in which case, check if you've selected the right Jira instance in the connection. 

#### 6. Why am I not able to select 'Next' in the create connection screen even after entering and setting up the correct information about my Jira instance? 

The **Next** button in the Create connection screen will be enabled only when authentication is done successfully. After entering your Jira credentials, check if you've authenticated the connection and clicked on the **Allow** option in the consent pop-up. Once you're authenticated successfully, the **Next** button will be enabled automatically. 

> [!NOTE]
> If you think all of the above are properly set up, please reach out to the Viva Goals support team via in-app chat or email us at support@ally.io for more information. 

## Troubleshooting guidelines for issues in the Viva Goals - Jira (Plugin) Integration

#### 1. While creating a Jira connection, I'm seeing the error message: “Service Unavailable”

Here are a few settings to check: 

- **Is the Jira server URL provided valid and accessible?** 

    Check if the Jira server URL you've provided follows this format: http://myjirapp.com/ and is reachable on HTTPS port. 

- **Is the Jira plugin installed successfully?**

    Check if the Jira plugin has been installed correctly. 

- **Are the configuration details you've given correct?**  

    Make sure the UUID and the access token you've provided in Viva Goals are correct. 

#### 2. Why I'm seeing a new user added in the Jira user settings? 

On successful authentication, Viva Goals creates a user within your Jira instance to be able to connect to Jira and update the data from Jira to Viva Goals. 

#### 3. What are the supported versions for the Jira Plugin-based integration? 

The Viva Goals - Jira plugin-based integration will work for Jira versions starting from 7.13.0 to 8.12.3. 

#### 4. Why am I not able to select 'Next' in the create connection screen even after entering and setting up the correct information about my Jira instance? 

The **Next** button in the Create connection screen will be enabled only when authentication is done successfully. After entering your Jira credentials, check if you've authenticated the connection and clicked on the **Allow** option in the consent pop-up. Once you're authenticated successfully, the 'Next' button will be enabled automatically. 