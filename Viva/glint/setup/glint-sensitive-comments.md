---
title: Flag Sensitive comments in Viva Glint
description: Sensitive comment flagging in Microsoft Viva Glint surfaces comments in the admin view of the Comments report that contain personally identifiable information (PII), sensitive topics, and profanity.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: sensitive comments, comment flagging
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high pri
ms.date: 09/20/2023
---

# Flag Sensitive comments in Viva Glint

Sensitive comment flagging in Microsoft Viva Glint surfaces comments in the admin view of the Comments report that contain personally identifiable information (PII), sensitive topics, and profanity. Admins can also quarantine and redact flagged comments in the Comments report when this feature is enabled.

## Sensitive comment categories

Flagged sensitive comments fall into 3 categories:

1. **Profanity:** Curse words and explicit language.
1. **Personally identifiable information (PII):** Personally identifiable information, like names.
1. **Sensitive work environment:** Keywords related to discrimination, harassment, unsafe working conditions, and bullying.

> [!NOTE]
> Sensitive comment flagging doesn't currently support non-English comments. 

## Enable sensitive comment flagging

To enable sensitive comments:

1. From the admin dashboard, select the **Configure** symbol, then in **Service Configuration**, choose **Advanced Configuration**.
1. Select **Surveys** and choose a survey.
1. In the **Sensitive Comments** section, select checkboxes for:
   1. Flag PII
   1. Flag Sensitive
   1. Flag Profanity
1. Select **Save Changes**.

> [!IMPORTANT]
> This update flags new comments, but doesn't flag feedback submitted before enabling sensitive comments.

## Manage sensitive comments as an admin

With sensitive comment flagging enabled, admins see 4 additional categories in their Comments report: PII, Profanity, Sensitive, and Quarantined. There are also **Redact All Terms** and **Un-Redact All** options available for redacting flagged words in bulk.

### Quarantine comments

Quarantined comments are hidden from non-admin users. To quarantine a flagged comment:

1. From the admin dashboard, select **Reports**, then choose **Comments**.
1. In the **Comments** section, go to the **PII**, **Profanity**, or **Sensitive** sections to view flagged comments. Keywords are highlighted in red.
1. On each comment, select the ellipsis (...) and choose **Quarantine** to move comments to the Quarantined category.
1. To remove a comment from the Quarantined category, select the ellipsis (...) and choose **Un-Quarantine**.

### Redact comments

To replace PII and profanity in flagged comments with "#####", choose to redact in bulk or for specific comments.

> [!NOTE]
> Flagged keywords for comments in the **Sensitive** category can't be redacted.

To redact all PII and profanity terms:

1. From the admin dashboard, select **Reports**, then choose **Comments**.
1. In the **Comments** section, select **Redact All Terms** to mask flagged words with "#####" for all comments.
1. Select **Un-Redact All** to restore the original comment text.

To redact PII and profanity for specific comments:

1. From the admin dashboard, select **Reports**, then choose **Comments**.
1. In the **Comments** section, go to the **PII** or **Profanity** sections to view flagged comments. Keywords are highlighted in red.
1. On each comment, select the ellipsis (...) and choose **Redact**.
1. To restore the original comment text, select the ellipsis (...) and choose **Un-Redact**.
