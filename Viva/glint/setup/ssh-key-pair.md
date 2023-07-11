---
title: Create an SSH key pair for SFTP
description: To access your Microsoft Viva Glint SFTP account, create an SSH key pair, which includes a public and private key.  
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: SFTP, public SSH key, SSH key pair
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/10/2023
---

# Create an SSH key pair for SFTP

To access your Microsoft Viva Glint SFTP account, create an SSH key pair, which includes a public and private key.

> [!NOTE]
> In addition to a public SSH key, to connect to SFTP, also enter the public IP address(es) for accounts that will connect to SFTP so that they can be added to a Viva Glint allowed list as valid users. [Configure SFTP IP addresses in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2238339).

## Understand SSH key pair requirements

To connect to your Viva Glint SFTP account, ensure that the SSH key pair:

- Has a key length of at least 2048, ideally 4096 bits.
- Has type RSA in OpenSSH format.

> [!TIP]
> Passphrases are optional for key files. To omit, leave blank when prompted.

## Create an SSH key pair on Microsoft Windows

To create a key pair on Microsoft Windows operating systems:

1. Download PuTTy Key Generator [PuTTYgen.exe](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html) file and run it.
2. In the **Key** menu, select **SSH-2 RSA key**.
3. In **Parameters** , select the **RSA** option.
4. In the **Number of bits in a generated key field** , enter at least 2048, ideally 4096.
5. In **Actions** , select **Generate**.
6. A progress bar will appear. In the blank area below, move your pointer in a random pattern to complete key pair generation.
7. When generation completes, **copy** the contents of the _Public key for pasting into OpenSSH authorized\_keys file_ field and **paste** into a text editor application (like Notepad).
8. **Save** your file as **vivaglint-yyyymmdd.pub**.
9. _Key passphrase_ and _Confirm passphrase_ fields aren't required, leave fields blank for no passphrase.
10. Select **Save private key** tosavetheprivate key file. This will be the key you import into a File Transfer Protocol (FTP) application to connect to Viva Glint SFTP.

## Create an SSH key pair on Macintosh or Linux

To create a key pair on Macintosh or Linux operating systems:

1. Open a **Terminal** window. In Macintosh operating systems, find **Terminal** in the **Dock** or in the **Utilities** folder.
2. Enter the following command: **ssh-keygen -b 2048 -t rsa -C "your\_username" -f filename**
   1. The length, determined by **-b** , should be _at least_ 2048, but ideally 4096 bits.
   2. Update **your\_username** and **filename** values.
   3. Example: **ssh-keygen -b 2048 -t rsa -C** "**jsmith**" -**f**  **vivaglint-yyyymmdd**
3. Select **enter** and follow prompts.
4. A passphrase isn't required. Supply a passphrase if desired or leave blank and continue.
5. When successfully generated, you'll see:
   - Your identification has been saved in filename
   - Your public key has been saved in filename.pub
6. **Search** for the public and private key files in **Finder**.
   1. The two key files will be named what is specified in the Terminal command.
      - Example: _vivaglint-yyyymmdd\_key_ and _vivaglint-yyyymmdd\_key.pub_.
   2. With no specified file name, the key files will appear as: _id\_rsa_ and _id\_rsa.pub_.
