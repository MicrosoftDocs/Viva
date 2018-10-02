---
# Metadata Sample
# required metadata

title: Configure settings for Workplace Analytics
description: Describes how Workplace Analytics administrators can set and edit settings in Workplace Analytics. 
author: madehmer
ms.author: v-johtob
ms.date: 07/20/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Configure settings for Workplace Analytics

On the Settings page, administrators can customize system defaults and privacy settings, and upload organizational data to Workplace Analytics.

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa.md)]

## Time zone settings
In the **System defaults** section, you can customize the **Default time zone**. This is used to compute after-hours metrics for employees whose time zone was not provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time. Visit [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md) for a complete list of times zones you can use.

![Default time zone](../images/Wpa/use/default-timezone-settings.png)

### To change the default time zone

1. On the **Settings** page, select **Settings**.
2. Under **System defaults**, select a time zone from the **Default time zone list**.
3. Select **Save**.

This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

## Privacy settings

In the **Privacy settings** section, you can customize and configure what data is accessible for analysis.

> [!Note]
> When adding the subject line words to exclude from analysis, use single words, separated by a semicolon.

### What you can do with privacy settings

* Specify the smallest group size to appear in the Explore Metrics section. Larger group sizes reduce the risk of individual group members being personally identified.
* Specify whether subject lines should be shown in query results.
* Exclude sensitive emails, domains, or keywords in subject lines.

Learn more about [Workplace Analytics privacy and data access](../privacy/privacy-and-data-access.md).

When you are satisfied with your privacy settings, your data can be processed.

![Privacy settings](../images/Wpa/use/privacy-settings-settings.png)

### To configure your privacy settings

1. On the **Settings** page, select **Settings**.
2. Under **Privacy settings**, configure the settings to meet your company's needs.

 > [!Note]
 > You may select **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you select the **I confirm that all privacy settings are complete** check box. When you select the check box, it begins the processing of Office 365 data.

3. Select **Save**.

 > [!Note]
 > Carefully validate that your privacy settings are correct, before you select the **I confirm that all privacy settings are complete** check box. You can change the settings at any time, but the setting changes will not take effect until the data is processed by Office 365 again for the following month.

4. To begin the processing of Office 365 data, select the **I confirm that all privacy settings are complete** check box, and then select **Save**.

### To begin processing your data in Workplace Analytics

* Select the **I confirm all privacy settings are complete** check box, and then select **Save**.

## Organizational data

Administrators will use the **Organizational data** tab to upload data into Workplace Analytics.

![Privacy settings](../images/Wpa/use/organizational-data-settings.png)

### To prepare your data for upload to Workplace Analytics

* Follow the instructions in [Prepare and upload organizational data](../setup/upload-organizational-data.md).