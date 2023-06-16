---
title: Configure SFTP IP addresses in Viva Glint 
description: "To connect to your Viva Glint Secure File Transfer Protocol (SFTP) account to transmit employee data, admin users need to maintain a list of valid public IP addresses."
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva-goals
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high pri
ms.date: 04/28/2023
---

# Configure SFTP IP addresses in Viva Glint 

To connect to your Viva Glint Secure File Transfer Protocol (SFTP) account to transmit employee data, admin users need to maintain a list of valid public IP addresses in General Settings. Only users with public IP addresses specified in your configuration settings are permitted to access your Viva Glint hosted SFTP account.  

## Determine public IP addresses for your organization 

Find public IP addresses with utilities such as: [https://ifconfig.io/](https://ifconfig.io/). Any user account that connects to your Viva Glint SFTP account must have a corresponding valid public IP address in Viva Glint General Settings in order to authenticate. Your organization may see connections from your: 

- Human Resources Information System (HRIS) tenants 
- Individual users 

Work with your HR, data automation, and/or IT departments to collect a list of valid public IP addresses.

>[!IMPORTANT]
> Private IP ranges are not internet routable per IPv4 protocol and will not allow SFTP connection. In your configuration, do not include private IP addresses which fall into these ranges:
> - **10.0.0.0/8 IP addresses**: 10.0.0.0 – 10.255.255.255 
> - **172.16.0.0/12 IP addresses**: 172.16.0.0 – 172.31.255.255
> - **192.168.0.0/16 IP addresses**: 192.168.0.0 – 192.168.255.255

## Manage public IP addresses in General Settings 

To edit the public IP addresses associated with your Viva Glint SFTP account: 

1. From the admin dashboard, select the **Configure** symbol, then in **Client Settings**, choose **General Settings**. 
2. In the **Technical Configuration** menu, in **SFTP Setup**, select **Manage**. 
3. In the configuration panel, add or remove your public IP address(es) in the **SFTP IP Addresses** field. 
   >[!NOTE]
   > Add multiple IP addresses in a comma-separated list.
 
4. At the top right of the panel, select **Save**. 
5. Allow one hour before testing a connection from a newly added IP address.  