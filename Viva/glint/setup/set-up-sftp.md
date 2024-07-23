---
title: Set up Secure File Transfer Protocol (SFTP) in Viva Glint
description: Use Microsoft Viva Glint Secure File Transfer Protocol (SFTP) to establish regular, automated imports of employee data.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: sftp, public ip address, pgp encryption, data transfer, ssh key
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 07/12/2024
---

# Set up Secure File Transfer Protocol (SFTP) in Viva Glint

Use Microsoft Viva Glint [Secure File Transfer Protocol (SFTP)](https://go.microsoft.com/fwlink/?linkid=2247429) to establish regular, automated imports of employee data. In Viva Glint General Settings, import SSH Public Keys, specify public IP addresses to connect (optional), specify users that should be notified about data uploads and warnings, opt-in to PGP encryption (optional), and view your credentials to access your SFTP account.  

Your IT team may need to add an IP exception or add hosts and ports to an allow list to connect to SFTP. [Learn more](https://go.microsoft.com/fwlink/?linkid=2238617). 

Learn more about how to set up SFTP with this video and the guidance in this article:
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1jOMv]

## Manage SFTP in General Settings

Manage SFTP settings to connect to your Viva Glint SFTP account:

1. From the admin dashboard, select the **Configuration** symbol, then in **Service Configuration**, choose **General Settings**.
1. In the **Technical Configuration** section, go to **SFTP Setup** and select **Manage**.
1. In the SFTP pane that appears, review each field and enter information as needed:

|Setup item   |Required or optional   |More information   |
|:----------|:-----------|:-----------|
|**SSH Public Key**     |Required       |<ul><li>Enter the full text of your public SSH key: `ssh-rsa ...` .</li><li>**DO NOT** share your private key with Viva Glint.</li><li>To generate a key pair, see: [Generate an SSH key pair](https://go.microsoft.com/fwlink/?linkid=2247507).</li><li>To convert a key to the required format, see: [Convert a key to OpenSSH format](convert-ssh-key.md).</li><li>Add up to three public SSH keys.</li></ul>       |
|**SFTP IP Addresses**     |Optional       |<ul><li>**Leave this field blank to allow any account to connect.**</li><li>Specify public IP addresses to limit accounts that can connect.</li><li>Contact your IT team, HRIS vendor, or use [online tools](https://ifconfig.io/) to determine your public IP address(es).</li><li>This field supports subnets, or ranges of IP addresses. Enter ranges (for example: 1.1.1.0/24) rather than individual IP addresses in each field, if needed.</li></ul>     |
|**Notify People**     |Required       |<ul><li>Search for and add users that should receive file upload notification emails.</li><li>Users must be active and exist in Viva Glint.</li></ul>       |
|**PGP Encryption**     |Optional       |<ul><li>Switch toggle to **On** to enable file encryption and reveal Glint's public PGP key to encrypt employee data files.</li><li>When this setting is enabled, SFTP accepts files with and without encryption.</li></ul>      |
|**SFTP Credentials**     |Required       |<ul><li>Use the credentials shown in the platform to connect to SFTP. Allow at least one hour after entering public SSH keys and IP addresses (optional) before testing your connection.</li><br><br><li>**File Protocol**: _SFTP_</li><li>**Port**: Select 22 or 1122</li> <li>**Host Name**: _Varies based on region (US or EU) and selected port_</li> <li>**Username:** _Company ID_</li> <li>**Password:** _Not applicable, use your private SSH key file_</li></ul>        |

> [!IMPORTANT]
> Private IP ranges aren't internet routable and don't allow SFTP connection. Don't include private IP addresses, which fall in these ranges:
> - **10.0.0.0/8 IP addresses:** 10.0.0.0 – 10.255.255.255
> - **172.16.0.0/12 IP addresses:** 172.16.0.0 – 172.31.255.255
> - **192.168.0.0/16 IP addresses:** 192.168.0.0 – 192.168.255.255
 
> [!NOTE]
> Once a tenant is deprovisioned or considered in a "LockedOut" state, the public SSH key is deleted and SFTP will no longer work.
