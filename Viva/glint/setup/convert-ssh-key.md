---
title: Convert a public SSH key to OpenSSH format for Viva Glint SFTP
description: If your organization can't generate a key pair in OpenSSH format, use these instructions to convert the SSH public key to the correct format.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: public key, SSH key, SFTP, OpenSSH, SSH
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/23/2024
---

# Convert a public SSH key to OpenSSH format for Viva Glint SFTP

To connect to your Microsoft Viva Glint SFTP account, the SSH key pair that your organization (or an HRIS vendor) generates needs:

- A key length of as least 2048, ideally 4096 bits.
- To be type RSA in **OpenSSH format**.

To create a key pair for an individual user that follows these guidelines, see: [Create an SSH key pair](sftp-ssh-key-gen.md). If your organization has an HRIS vendor that connects to Viva Glint SFTP and can't generate a key pair in OpenSSH format, use these instructions to convert the SSH public key to the correct format.

An OpenSSH public key (RSA type) should look similar to this example, and always start with 'ssh-rsa':

`ssh-rsa AAAA.....1ng3pj`

> [!NOTE]
> PGP keys are designed to encrypt data files and not to access SFTP. PGP keys can't be converted to OpenSSH format. To encrypt data files with Viva Glint's PGP public key, copy your organization's PGP key from SFTP setup in General Settings. [Learn more](set-up-sftp.md).

## Convert to OpenSSH format on Microsoft Windows

### OpenSSH2 format

What your key file looks like:

```
---- BEGIN SSH2 PUBLIC KEY ----
Comment: "rsa-key-20240201"
AAAAB..........vlsRMQ==
---- END SSH2 PUBLIC KEY ----
```

To convert to OpenSSH format:

1. Save the public key as a .pub file to a location on your computer with a text editor, like Notepad. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Command Prompt** and enter: `cd file location`. 
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. Copy and paste this command into Command Prompt: `ssh-keygen -i -f filename.pub > new-filename.pub`
5. Replace `filename` with the name of your public key file and select **enter**.
6. Command Prompt generates a converted, OpenSSH version of the public key in a new file.
7. Open File Explorer and search for `new-filename`.pub and open the file in a text editor, like Notepad.
8. Copy and paste the full text of the key from Notepad, including `ssh-rsa`.
9. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.

### OpenSSL format

What your key file looks like:

```
-----BEGIN PUBLIC KEY-----
MIIB..........AB
-----END PUBLIC KEY-----
```

or

```csharp
-----BEGIN RSA PUBLIC KEY-----
MIIB..........AB
-----END RSA PUBLIC KEY-----
```

To convert to OpenSSH format:

1. Save the public key as a .pem file to a location on your computer with a text editor, like Notepad. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Command Prompt** and enter: `cd file location`. 
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. Copy and paste this command into Command Prompt: `ssh-keygen -i -f filename.pub > new-filename.pub`
5. Replace `filename` with the name of your public key file and select **enter**.
6. Command Prompt generates a converted, OpenSSH version of the public key in a new file.
7. Open File Explorer and search for `new-filename`.pub and open the file in a text editor, like Notepad.
8. Copy and paste the full text of the key from Notepad, including `ssh-rsa`.
9. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.

### PKI format

What your key file looks like:

```
-----BEGIN PUBLIC KEY-----
xsBNBF.....L1AItI=
-----END PUBLIC KEY-----
```

or

```
-----BEGIN CERTIFICATE-----
xsBNBF.....L1AItI=
-----END CERTIFICATE-----
```

To convert to OpenSSH format:

1. Save the public key as a .cer file to a location on your computer with a text editor, like Notepad. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Command Prompt** and enter: `cd file location`. 
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. To separate the public key from the file, copy and paste this command into Command Prompt: `openssl x509 -in filename.cer -pubkey -noout > filename.pub.tmp`
5. Replace `filename` with the name of your public key file and select **enter**.
6. To convert the separated public key file to OpenSSH format, copy and paste this command into Command Prompt: `ssh-keygen -i -f filename.pub.tmp > filename.pub`
7. Replace `filename` with the name of your separated public key file and select **enter**.
8. Command Prompt generates a converted, OpenSSH version of the public key in a new file.
9. Open File Explorer and search for `filename`.pub and open the file in a text editor, like Notepad.
10. Copy and paste the full text of the key from Notepad, including `ssh-rsa`.
11. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.

### DER binary format

What your key file looks like:

`0<82>^BÜ0<82>^AÄ ^C^B^A^B^B^P^_mÔ=°^M<<95>I Ë^Q^E?ûí0^M^F *<86>H<86>÷^M^A^A^K^E^@0*1(0&^F^CU^D^C^S^_ADFS Signing -`

To convert to OpenSSH format:

1. Save the public key as a .cer file to a location on your computer with a text editor, like Notepad. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Command Prompt** and enter: `cd file location`. 
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. To convert to a format that can be converted to OpenSSH, copy and paste this command into Command Prompt: `openssl x509 -inform der -in filename.cer -out filename.pem`
5. Replace `filename` with the name of your public key file and select **enter**.
6. To separate the public key from the file, copy and paste this command into Command Prompt: `openssl x509 -in filename.cer -pubkey -noout > filename.pub.tmp`
7. Replace `filename` with the name of your public key file and select **enter**.
8. To convert the separated public key file to OpenSSH format, copy and paste this command into Command Prompt: `ssh-keygen -i -f filename.pub.tmp > filename.pub`
9. Replace `filename` with the name of your separated public key file and select **enter**.
10. Command Prompt generates a converted, OpenSSH version of the public key in a new file.
11. Open File Explorer and search for `filename`.pub and open the file in a text editor, like Notepad.
12. Copy and paste the full text of the key from Notepad, including `ssh-rsa`.
13. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**. 

## Convert to OpenSSH format on Macintosh or Linux

### OpenSSH2 format

What your key file looks like:

```
---- BEGIN SSH2 PUBLIC KEY ----
Comment: "rsa-key-20240201"
AAAAB..........vlsRMQ==
---- END SSH2 PUBLIC KEY ----
```

To convert to OpenSSH format:

1. Save the public key as a .pub file to a location on your computer with a text editor, like Sublime. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Terminal** and enter: `cd file location`. 
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. Copy and paste this command into Terminal: `ssh-keygen -i -f filename.pub`
5. Replace `filename` with the name of your public key file and select **enter**.
6. Terminal generates a converted, OpenSSH version of the public key.
7. Copy and paste the full text of the key from Terminal, including `ssh-rsa` into a text editor, like Sublime.
8. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.


### OpenSSL format

What your key file looks like:

```
-----BEGIN PUBLIC KEY-----
MIIB..........AB
-----END PUBLIC KEY-----
```

or

```
-----BEGIN RSA PUBLIC KEY-----
MIIB..........AB
-----END RSA PUBLIC KEY-----
```

To convert to OpenSSH format:

1. Save the public key as a .pem file to a location on your computer with a text editor, like Sublime. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Terminal** and enter: `cd file location`.
3. Replace `file location` and select enter to go to the folder where your key file is saved. 
4. Copy and paste this command into Terminal: `ssh-keygen -f filename.pem -i -m PKCS8 > filename.pub`
5. Replace `filename` with the name of your public key file and select **enter**.
6. Terminal generates a converted, OpenSSH version of the public key. 
7. Open Finder and search for `filename`.pub to find the converted version of your key file.
8. Open the .pub file in a text editor, like Sublime. 
9. Copy and paste the full text of the key, including `ssh-rsa`.
10. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.

### PKI format

What your key file looks like:

```
-----BEGIN PUBLIC KEY-----
xsBNBF.....L1AItI=
-----END PUBLIC KEY-----
```

or

```
-----BEGIN CERTIFICATE-----
xsBNBF.....L1AItI=
-----END CERTIFICATE-----
```

To convert to OpenSSH format:

1. Save the public key as a .cer file to a location on your computer with a text editor, like Sublime. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Terminal** and enter: `cd file location`.
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. To separate the public key from the file, copy and paste this command into Terminal: `openssl x509 -in filename.cer -pubkey -noout > filename.pub.tmp`.
5. Replace `filename` with the name of your public key file and select **enter**.
6. To convert the separated public key file to OpenSSH format, copy and paste this command into Terminal: `ssh-keygen -f filename.pub.tmp -i -m PKCS8 > filename.pub`
7. Replace `filename` with the name of your separated public key file and select **enter**.
8. Open Finder and search for `filename`.pub to find the converted version of your key file.
9. Open the .pub file in a text editor, like Sublime. 
10. Copy and paste the full text of the key, including `ssh-rsa`.
11. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.

### DER binary format

What your key file looks like:

`0<82>^BÜ0<82>^AÄ ^C^B^A^B^B^P^_mÔ=°^M<<95>I Ë^Q^E?ûí0^M^F *<86>H<86>÷^M^A^A^K^E^@0*1(0&^F^CU^D^C^S^_ADFS Signing -`

To convert to OpenSSH format:

1. Save the public key as a .cer file to a location on your computer with a text editor, like Sublime. 

   > [!IMPORTANT]
   > Don't include spaces in the file name.

2. Open **Terminal** and enter: `cd file location`.
3. Replace `file location` and select enter to go to the folder where your key file is saved.
4. To convert to a format that can be converted to OpenSSH, copy and paste this command into Terminal: `openssl x509 -inform der -in der_certificate.cer -out certificate.pem`
5. Replace `certificate` with the name of your public key file and select **enter**.
6. To separate the public key from the file, copy and paste this command into Terminal: `openssl x509 -in filename.cer -pubkey -noout > filename.pub.tmp`.
7. Replace `filename` with the name of your public key file and select **enter**.
8. To convert the separated public key file to OpenSSH format, copy and paste this command into Terminal: `ssh-keygen -f filename.pub.tmp -i -m PKCS8 > filename.pub`
9. Replace `filename` with the name of your separated public key file and select **enter**.
10. Open Finder and search for `filename`.pub to find the converted version of your key file.
11. Open the .pub file in a text editor, like Sublime. 
12. Copy and paste the full text of the key, including `ssh-rsa`.
13. Paste the new public key text into the **SSH Public Key** field in Viva Glint **SFTP Setup**.
