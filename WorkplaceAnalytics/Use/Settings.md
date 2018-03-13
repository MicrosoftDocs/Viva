---
# Metadata Sample
# required metadata

title: Configure settings for Workplace Analytics
description: This articles decribes how Workplace Analytics administrators can set and edit settings in Workplace Analytics. 
author: rodonahu
ms.author: rodonahu
ms.date: 01/19/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Configure settings for Workplace Analytics
On the **Settings** page, administrators can customize system defaults and privacy settings, and upload organizational data to Workplace Analytics. There are two tabs, **Settings** and **Organizational data**.



## Timezone settings

In the **System defaults** section, you can customize the **Default time zone**. This is used to compute after-hours metrics for employees whose   time zone was not provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time. Visit [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md) for a complete list of times zones you can use.

![Default time zone](../images/Wpa/use/default-timezone-settings.png)


### To change the default time zone
1.	On the **Settings** page, click **Settings**.
2.	Under **System defaults**, select the time zone you want from the **Default time zone** menu.
3.	Click **Save**.

This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

## Privacy settings

In the **Privacy settings** section, you customize and configure what data is accessible for analysis.

> [!Note]
> When adding the subject line words to exclude from analysis, use single words, separated by a semicolon.


### With privacy settings you can
* Specify the smallest group size to appear in the Explore Metrics section. Larger group sizes reduce the risk of individual group members being personally identified.
* Specify whether subject lines should be shown in query results.
* Exclude sensitive emails, domains, or subject line keywords.

Learn more about [Workplace Analytics privacy and data access](../overview/privacy-and-data-access.md).

When you are satisfied with your privacy settings, your data can be processed.

![Privacy settings](../images/Wpa/use/privacy-settings-settings.png)


### To configure your privacy settings
1.	On the **Settings** page, click **Settings**.
2.	Under **Privacy settings**, configure the settings to meet your company's needs.


> [!Note]
> You may click **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you click the **I confirm that all privacy settings are complete** checkbox. When you click the checkbox, it begins the processing of Office 365 data.

3.	Click **Save**.

> [!Note]
> Carefully validate that your privacy settings are correct, before you click the **I confirm that all privacy settings are complete** checkbox, You can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.

4.	To begin the processing of Office 365 data, click the **I confirm that all privacy settings are complete checkbox**, and then click **Save**.

### To begin processing your data in Workplace Analytics
* Check the **I confirm all privacy settings are complete** checkbox, and then click **Save**.

## Organizational data
Administrators will use the **Organizational data** tab to upload your data into Workplace Analytics.

![Privacy settings](../images/Wpa/use/organizational-data-settings.png)


### To prepare your data for upload
* Follow the instructions in the topic [Prepare and export organizational data for Workplace Analytics](../use/Prepare-and-upload-organizational-data.md).
