---
title: Create an SSH key pair
description: To access your Microsoft Viva Glint SFTP account, create an SSH key pair, which includes a public and private key. 
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: sftp, public ssh key, ssh key pair
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/29/2024
---

# Create an SSH key pair

To access your Microsoft Viva Glint (Secure File Transfer Protocol) SFTP account, create an SSH key pair, which includes a public and private key.

> [!NOTE]
> These instructions are for individual users that connect to Viva Glint SFTP. Your organization may have an HR information system (HRIS) connect directly to SFTP to send employee data. Work with your HRIS team to have a SSH key pair generated for the HRIS to allow it to connect.

## Understand SSH key pair requirements

To connect to your Viva Glint SFTP account, ensure that the SSH key pair:

- Has a key length of as least 2048, ideally 4096 bits.
- Is type RSA in OpenSSH format.

> [!IMPORTANT]
> If your organization or HRIS vendor can't generate a key pair in OpenSSH format, [convert the public SSH key to OpenSSH format](convert-ssh-key.md) before adding to Viva Glint.

> [!TIP]
> Passphrases are optional for key files. To omit, leave blank when prompted.

## Create an SSH key pair on Microsoft Windows

To create a key pair on Microsoft Windows operating systems:

1. Download PuTTy Key Generator [PuTTygen.exe file](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) and run it.
1. In the **Key** menu, select **SSH-2 RSA Key**.
1. In **Parameters**, select the **RSA** option.
1. In **Number of bits in generated key field**, enter at least 2048, ideally 4096.
1. In **Actions**, select **Generate**.
1. A progress bar appears. In the blank area under the bar, move your pointer in a random pattern to complete key pair generation.
1. When generation completes, copy the contents of the **Public key for pasting into OpenSSH authorized_keys file** field and past into a text editor application (like Notepad).
   > [!IMPORTANT]
   > Copy the _**full text**_ of the public key, including `ssh-rsa`, into the SSH Public Key field when you [set up SFTP in General Settings](set-up-sftp.md).
1. Save your file as **vivaglint-yyyymmdd.pub**.
1. **Key passphrase** and **Confirm passphrase** fields aren't required. Leave blank for no passphrase.
1. Select **Save private key** to save the private key file. This key lets you connect to SFTP in a dedicated FTP application.

## Create an SSH key pair on Macintosh or Linux

To create a key pair on Macintosh or Linux operating systems:

1. Open a **Terminal** window. in Macintosh operating systems, find **Terminal** in the **Dock** or in the **Utilities** folder.
1. Enter the following command: `ssh-keygen -b 2048 -t rsa -C "your_username" -f filename`.
   1. The length, determined by -b, should be at least 2048, ideally 4096.
   1. Update **your_username** and **filename** values. 
   1. Example: `ssh-keygen -b 2048 -t rsa -C "jsmith" -f vivaglint-yyyymmdd`.
1. Select **enter** and follow prompts.
1. A passphrase isn't required. Supply a passphrase or leave blank and select **enter** to continue.
1. When successfully generated, you see these messages:
   1. Your identification has been saved in **filename**.
   1. Your public key has been saved in **filename.pub**.
1. Search for the public and private key files in **Finder**.
   1. The two key files are named based on what was specified in the Terminal command.
      1. Example: **vivaglint-yyyymmdd** and **vivaglint-yyyymmdd.pub**
   1. With no specified file name, the key files appear as: **id_rsa** and **id_rsa.pub**.
1. Open the .pub file (the SSH public key) in a text editor (like TextEdit) and copy the contents.
   > [!IMPORTANT]
   > Copy the _**full text**_ of the public key, including `ssh-rsa`, into the SSH Public Key field when you [set up SFTP in General Settings](set-up-sftp.md).

