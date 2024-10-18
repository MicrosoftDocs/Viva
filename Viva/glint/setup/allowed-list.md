---
title: Allowlist information for Viva Glint
description: Add approved domains, IPs, and ports, which can be different depending on your account's region, to your organization's allowlist.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: approved sender, allowed list, firewall, spam, allowlist
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/14/2024
---

# Allowlist information for Viva Glint

Microsoft Viva Glint operates in two distinct geographical regions: the United States (US) and in the European Union (EU). Add approved domains, IP addresses, and ports, which can be different depending on your account's region, to your organization's allowlist. Viva Glint recommends that you add **full domains,** and not the specific addresses. For example, to ensure users receive invites from no-reply@glint.mail.microsoft, add **glint.mail.microsoft** to your allowed list.

## Add email sender domains

Viva Glint emails come from one of the domains listed here for the US and EU. Add the following domains to your allowlist:

- glint.mail.microsoft - Survey Notifications
- microsoft.com - Microsoft Email Communications
- email1.microsoft.com - Newsletter and Product Updates

#### Glint survey and system emails for the US and EU originate from:

- **no-reply@glint.mail.microsoft**

## Logos and images

Confirm that your email service permits Viva Glint emails to display images for **logos** to render. Some third-party email applications have security restrictions in place that block the download of images into an email. Ensure that automatic image downloads from external senders are allowed. If your organization uses [custom company branding](/entra/fundamentals/how-to-customize-branding), images download automatically.

## Spam gateways

If there are any **Spam gateways** on your exchange server, ensure that they're configured to successfully receive survey emails in bulk from Viva Glint without causing throttling, delays, or bounce backs.

## Inbox filtering

Some email providers have **special inboxes that automatically filter** certain types of mail. To ensure email from Viva Glint arrives in employees' primary inbox, review your application or exchange server settings.

## Allow application hosts and ports

Your organization may require domains or URLs to be opened to access Viva Glint's application. The following hosts and ports need to be allowed, depending on which region your account resides in.

### United States:

| Host | TCP port | Description |
| :--- | :--- | :--- |
| sftp2.us1.glint.cloud.microsoft | 22 | Secure File Transfer Protocol |
| sftp.us1.glint.cloud.microsoft | 1122 | Secure File Transfer Protocol |
| www.microsoft.com | 443 | Viva Glint Website (US and EU) |
| techcommunity.microsoft.com | 443 | Viva Glint Community |
| app.us1.glint.cloud.microsoft | 443 | Viva Glint website and Unified Login |
| api.us1.glint.cloud.microsoft | 443 | Viva Glint unified login |
| feedback.us1.glint.cloud.microsoft | 443 | Viva Glint survey landing page |

### European Union:

| Host | TCP port | Description |
| :--- | :--- | :--- |
| sftp2.eu1.glint.cloud.microsoft | 22 | Secure File Transfer Protocol |
| sftp.eu1.glint.cloud.microsoft | 1122 | Secure File Transfer Protocol |
| www.microsoft.com | 443 | Viva Glint Website (US and EU) |
| techcommunity.microsoft.com | 443 | Viva Glint Community |
| app.eu1.glint.cloud.microsoft | 443 | Viva Glint website and Unified Login |
| api.eu1.glint.cloud.microsoft | 443 | Viva Glint unified login |
| feedback.eu1.glint.cloud.microsoft | 443 | Viva Glint survey landing page |

## Admin consent for the Viva Glint Community

Your organization may need to take steps to allow users to post and reply to questions in user groups in the Viva Glint Community (techcommunity.microsoft.com). If users see a "Need admin approval" message when signing in, an IT administrator needs to grant the application access. [Learn more about admin consent](https://go.microsoft.com/fwlink/?linkid=2282450).

## Third-party cookies

Some Viva Glint applications require the use of **third-party cookies**, like hosted learning content. Should you receive an error saying that your browser is missing an authentication cookie, take appropriate steps to allow this third-party cookie.

## IP exceptions

If your organization requires an **IP exception** for Viva Glint's SFTP server, use the IP address based on your Viva Glint region (US or EU) and selected SFTP port (22 or 1122):

| Host | TCP port | IP address |
| :--- | :--- | :--- |
| sftp2.us1.glint.cloud.microsoft | 22 | 40.88.26.84 |
| sftp.us1.glint.cloud.microsoft | 1122 | 172.174.87.0 |
| sftp2.eu1.glint.cloud.microsoft | 22 | 52.138.180.95 |
| sftp.eu1.glint.cloud.microsoft | 1122 | 20.238.98.162 |
