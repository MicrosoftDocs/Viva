---
# Metadata Sample
# required metadata

title: Configure settings for Workplace Analytics
description: Describes how Workplace Analytics administrators can configure and edit settings in Workplace Analytics. 
author: buntus
ms.author: v-johtob
ms.date: 07/20/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Configure Workplace Analytics settings

## Workplace Analytics settings

On the **Settings** page, admins can customize system defaults and privacy settings and can also upload [organizational data](../Use/settings.md#organizational-data) to Workplace Analytics, from the respective tabs. This article focuses on system defaults and privacy settings. 

Use company-specific legal and privacy guidelines to define the settings to use in Workplace Analytics. After you define and confirm privacy settings, you are ready to provision the service to comply with these rules. 

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa.md)]

### System and privacy

On the **System and privacy** tab, in the **System defaults** section, you can configure the following employee options:

- Default time zone
- Working days and hours
- Hourly rate

#### Default time zone

This setting lets you configure the default time zone, which is used to compute after-hours metrics for employees whose time zone information was not originally provided in the organizational data file upload. Typically, the default time zone is the time zone of the corporate headquarters or the time zone in which most employees reside.

If a measured employee or other internal collaborator does not have a time zone defined in the organizational data file, or if you do not update the default time zone setting for your zone, Workplace Analytics uses Pacific Standard Time (PST).

#### To configure the default time zone

- From the **Default time zone** list box, under **System defaults**, select the appropriate time zone.

    ![System defaults](../images/WpA/Use/settings-default-time-zone-b.png)

### Working days and hours

Users can set their own working days and hours in [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).
Although no option exists within the organizational data file to upload working days and hours, Workplace Analytics administrators can set default working days and hours for the organization.

The **Working days and hours** setting lets admins specify the working and non-working days and hours of employees who have not already configured these settings in their mailbox.

  ![System defaults](../images/WpA/Use/settings-system-defaults-b.png)

#### To configure working days and hours

1. Under **Working days**, select the appropriate check boxes for the days of the week.
2. From the **Working day starts** and **Working day ends** list boxes, select the start and end times.

### Hourly rate

The **Hourly rate** field in **System defaults** is related to the optional **HourlyRate** column in the organizational data file that admins can choose to include. This column is used to calculate the total cost of low-quality meetings, as summarized on the [Meetings overview](../use/explore-metrics-meetings-overview.md#hourly-rate) page.

If you include the **HourlyRate** column in the organizational data file, cost is calculated as the sum of a person's default hourly rate for the organization multiplied by low-quality meeting hours.

The **Hourly Rate** field lets admins set the hourly rate for employees when required. If no hourly rate is assigned to a meeting participant in the organizational data file, the default hourly rate field in System defaults, is set to $75. However, admins can change the default value to any other hourly rate.

#### To configure the hourly rate

- Under System defaults, in the **Hourly rate** field, enter the appropriate employee hourly rate.

### Configure privacy settings

In the **Privacy settings** section, you can configure and customize the data that you want to include for analysis.

**You can use privacy settings to**:

- Specify the minimum group size. 

    The minimum group size setting determines what you can view in the visual dashboards in [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md) and in the [Solutions](../tutorials/solutions-task.md) area, and helps maintain employee privacy by ensuring that individuals cannot be easily identified by the attributes of the group. 
    The default minimum group size is set to five, but you can adjust the group size to suit the needs of your organization. However, you cannot set the size to lower than five. Larger group sizes reduce the risk of identification of individual group members.

- Specify whether to hide subject lines in [Meeting query](../tutorials/meeting-queries.md) results.

    This enables you to control whether to include or hide subject lines in meeting query results. By default, subject lines are _not_ shown in meeting query results. Subject lines are useful for analysts who want to set up meeting exclusion rules or query meeting data. You can decide to:

- Exclude instances of collaboration between:
    - Specific email addresses
    - Specific users in specific domains

    That is, you can exclude any emails and meetings emails to or from specific users, or exclude all users from specified domains, which helps to maintain employee privacy. Office 365 admins should not assign licenses to any excluded email addresses.

- Exclude words from subject lines

    This means you can exclude specific words from being displayed in the subject line of emails or meetings. Terms can be any combination of letters, numbers and special characters, for example, client attorney privilege; D&I.

   ![Privacy settings](../images/WpA/Use/settings-privacy-settings-b.png)

> [!Note]
> When specifying domains, email addresses, or subject line words to exclude from analysis, enter separate words in the corresponding fields, separated by a semicolon as the delimiter.  If you exclude email addresses, do not assign licenses to them.

Exclusion occurs before metadata is processed within Workplace Analytics. Learn more about [Workplace Analytics privacy and data access](../privacy/privacy-and-data-access.md).

### To configure privacy settings

1. Under **Privacy settings**, configure the minimum group size in the corresponding field.
2. Hide any desired meeting subject lines from query results in the corresponding drop-down menu. 
3. Exclude from analysis any domains, email addresses, or words from subject lines that you want.
4. Carefully verify that your privacy settings are correct and then select **"I confirm that all privacy settings are complete and that data will not be made available until user licenses have been applied**". Settings are not final until you select this check box.

3. At the top right of the page, select **Save**.

  Workplace Analytics only begins processing data when privacy settings run for the first time after you select **Save**. Processing your data can take up to two weeks to complete. Once the data is ready, you can then upload the organizational data file. Privacy settings take effect after the organizational data file is uploaded and processed.

   ![Privacy settings](../images/WpA/Use/settings-privacy-settings.png)

> [!Note] All subsequent changes to privacy
> settings after the first run, do not take effect until the next time that Workplace Analytics refreshes collaboration data. Any changes made to system defaults affect existing data.


## Organizational data

On the **Organizational data** tab, admins can upload an organizational data file to Workplace Analytic in .csv format. Organizational data is contextual information about employees (for example, job title, level, location) and can come from human resources or other information systems.
Changes to specific attributes in the organizational data file only take effect from their specified effective date. For information on preparing and uploading the organizational data file, see [Preparing organizational data](../Setup/prepare-organizational-data.md).


### Video: Privacy

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>
