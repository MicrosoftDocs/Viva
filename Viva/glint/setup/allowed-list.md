---
title: Review allowed list information for Viva Glint
description: Add approved domains, IPs, and ports, which can be different depending on your account's region, to your organization's allowed list.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: approved sender, allowed list, firewall, spam
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/30/2024
---

# Review allowed list information for Viva Glint

## What is an allowed list?

An allowed list is a list of preapproved URL or email addresses that receive guaranteed access to your server. An allowed list is a security feature to reduce unapproved access by allowing only trusted files, applications, and processes to be run.

## Manage your allowed list for Viva Glint

Viva Glint operates in two distinct geographical regions: the United States and in the European Union. Add approved domains, IP addresses, and ports, which can be different depending on your account's region, to your organization's allowed list. Viva Glint recommends that you add **full domains,** and not the specific addresses. For example, to ensure users receive invites from [no-reply@glint.microsoft.com](mailto:no-reply@glint.microsoft.com), add **glint.microsoft.com** to your allowed list.

## Add email sender domains

Viva Glint emails come from one of the domains listed here. Add the following domains to your allowed list:

### United States (US) and European Union (EU):

- glint.microsoft.com - Survey Notifications
- microsoft.com - Microsoft Email Communications
- email1.microsoft.com - Newsletter and Product Updates

### Glint survey and system emails originate from:

- US and EU: **no-reply@glint.microsoft.com** and **no-reply@glint.mail.microsoft**

## Take other steps to ensure email delivery

Confirm that your email service permits Viva Glint emails to display images for **logos** to render. Some third-party email applications have security restrictions in place that block the download of images into an email. Ensure that fd-glint-glintus1.azurefd.net (US) or fd-glint-glinteu1.azurefd.net (EU) are added as a trusted sender and that automatic image downloads from external senders are allowed.

If there are any **Spam gateways** on your exchange server, ensure that they're configured to successfully receive survey emails in bulk from Viva Glint without causing throttling, delays, or bounce backs.

Some email providers have **special inboxes that automatically filter** mail of a certain type. Review your application or exchange server settings to ensure email from Viva Glint arrives in the primary inbox for employees.

## Allow application hosts and ports

Your organization may require domains or URLs to be opened to access Viva Glint's application. The following hosts and ports need to be allowed, depending on which region your account resides in.

### United States:

| Host | TCP port | Description |
| --- | --- | --- |
| sftp2.us1.glint.cloud.microsoft | 22 | Secure File Transfer Protocol |
| sftp.us1.glint.cloud.microsoft | 1122 | Secure File Transfer Protocol |
| www.microsoft.com | 443 | Viva Glint Website (US and EU) |
| techcommunity.microsoft.com | 443 | Viva Glint Community |
| fd-glint-glintus1.azurefd.net | 443 | Viva Glint CDN |
| app.us1.glint.cloud.microsoft | 443 | Viva Glint website and Unified Login |
| api.us1.glint.cloud.microsoft | 443 | Viva Glint unified login |
| feedback.us1.glint.cloud.microsoft | 443 | Viva Glint survey landing page |

### European Union:

| Host | TCP port | Description |
| --- | --- | --- |
| sftp2.eu1.glint.cloud.microsoft | 22 | Secure File Transfer Protocol |
| sftp.eu1.glint.cloud.microsoft | 1122 | Secure File Transfer Protocol |
| www.microsoft.com | 443 | Viva Glint Website (US and EU) |
| techcommunity.microsoft.com | 443 | Viva Glint Community |
| fd-glint-glinteu1.azurefd.net | 443 | Viva Glint CDN |
| app.eu1.glint.cloud.microsoft | 443 | Viva Glint website and Unified Login |
| api.eu1.glint.cloud.microsoft | 443 | Viva Glint unified login |
| feedback.eu1.glint.cloud.microsoft | 443 | Viva Glint survey landing page |

## Explore more allowed list information

Some Viva Glint applications require the use of **third-party cookies**, such as hosted learning content. Should you receive an error saying that your browser is missing an authentication cookie, take appropriate steps to allow this third-party cookie.

If your organization requires the addition of an **IP exception** for Viva Glint's SFTP server, the US address is 172.174.87.0, and the EU address is 20.238.98.162.
