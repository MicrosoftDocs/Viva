---
title: Import historical response data in Viva Glint
description: For highly trained users, Microsoft Viva Glint Advanced Configuration offers the ability to import external, historical response data for items that trend with items that you select for your Viva Glint survey program.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: Advanced configuration, external import, historical response data, historical import
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 09/07/2023
---

# Import historical response data in Viva Glint

For highly trained users, Microsoft Viva Glint Advanced Configuration offers the ability to import external, historical response data for items that trend with items that you select for your Viva Glint survey program.

## Learn about the People Science perspective

It’s common for an organization to spend years asking the same survey items that leaders are comfortable with. It may be time to revisit items to ensure they're aligned to your organization’s current strategy. Before undertaking an import of historical, external data, consider these factors: [Learn more](https://go.microsoft.com/fwlink/?linkid=2245072).

## Review prerequisites

Data from an external source must meet the prerequisites listed here to be eligible for import to Viva Glint. If your data don't meet these requirements, do not import via the Advanced Configuration External Import feature.

### Survey program

- The confidentiality threshold for your Viva Glint survey program is equal to or greater than the source survey for the external data.
- Data are imported to a Recurring or Ad-Hoc survey.

> [!IMPORTANT]
> External imports are not available for Always-on or Lifecycle surveys.

### Survey items

- External data are tied to items that map to Viva Glint items. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230918).
- The response scale for rated items is compatible with Viva Glint:
  - 5-point Likert scale: 1 = Strongly Disagree, 2 = Disagree, 3 = Neither, 4 = Agree, 5 = Strongly Agree.
  - Reversed 5-point Likert scales require conversion before import to Viva Glint.

### Respondent data

- Raw, respondent-level data, **NOT** aggregated data.
- All respondents are identifited with their unique employee ID.
- External data attributes and values map to values in Viva Glint.
- The file layout aligns with Viva Glint requirements:
  - Horizontal layout with individual response data and attributes. See more details in the **Prepare data files** section.
 
## Map historical survey items

Complete a mapping of historical and Viva Glint items to determine exactly where you'll see trend in reporting. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230918).

> [!IMPORTANT]
> As you map items from the Question Library to historical items, include the Glint question ID, which is available in Question Library exports. You will need these IDs to prepare your Raw Score File.

## Set up a survey program

Set up your Viva Glint program, including items that trend with your external survey data. [Learn more](https://go.microsoft.com/fwlink/?linkid=2231504).

> [!TIP]
> Before importing users for the external import, select a placeholder Distribution List to complete program setup, such as Company Admin.

> [!NOTE]
> Exclusion lists and question targeting configured in your survey will not apply to an historical import.

## Prepare data files

External imports of historical data require three data files, each with their own requirements.

> [!IMPORTANT]
> All files must be in .csv format with a comma separator and UTF-8 encoding.

|File  |Description  |Email address label|Import to |
|----------|-----------|------------|------------|
|User File     |All employees from an historical, external source formatted to align with your Viva Glint attribute setup       |Match with your attribute setup        |Viva Glint People page        |
|Raw Score File|Respondent email address + question columns populated with numeric response values   |Must be: User e-mail|Advanced Configuration: External Import|
|Respondent User File|Required fields for all respondents from historical, external source: email, first name, last name, ID, status   |Must be: Email Address|Advanced Configuration: External Import|

### User File

To import historical data and generate reports, first add all historical employees to Viva Glint with an employee import. This file includes all employees from an historical, external source formatted to align with your Viva Glint attribute setup.

Comfirm that:

- Attribute setup is complete in Viva Glint. [Learn more](https://go.microsoft.com/fwlink/?linkid=2231504).
- Employee IDs and Email Addresses between current Viva Glint and historical users are aligned.
- You include accurate Employee ID and Manager ID relationships to calculate your manager hierarchy for historical data and reporting. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230861).
- Attributes and values between current Viva Glint and historical users are aligned. 
  - For example: Department = Human Resources will not trend with Department = HR.

### Raw Score File

Your Raw Score File should be in a horizontal layout and contain:

- Email as the first column which **must** be: User e-mail
- Question ID and comment columns (if open-ended feedback is included).
  - Use the Question IDs from the Question Mapping exercise that you conducted to assign Glint Question IDs to your historical response data.
  - Only include data for items that were mapped to Glint items and that you have added to your Glint survey program.
  - Ensure that Key Outcome items are included in your Raw Score File (for example: eSat and Recommend). If Viva Glint Key Outcome items don't exist in historical data, include the Question IDs as blank columns in your Raw Score File.
  - For comments associated with rating questions, place a column to the right of the question column and add **_COMMENTS** to the question ID, like the column C example.
  - For open-ended questions, use the same column layout, but populate 0 where there's a comment and -1 where there is no comment. See example in columns D and E.

> [!IMPORTANT]
> Comments that exceed 1024 characters will be truncated.

Sample:

|A  |B   |C|D|E|
|----------|-----------|------------|------------|------------|
|**User e-mail**     |**d31bf3a1-4c2f-4f9b-ba96-9dcede600477**      |**d31bf3a1-4c2f-4f9b-ba96-9dcede600477_COMMENTS**        |**f1c63ea9-5991-402a-bb06-06419ae78613**        |**f1c63ea9-5991-402a-bb06-06419ae78613_COMMENTS**        |
|ana.bowman@contoso.com|4   |My manager checks in with me often.|0 |Our company gives us a good worklife balance. |
|cameron.baker@contoso.com|5   | |-1 ||

### Respondent User File

Your Respondent User File needs to contain the following fields for the survey respondents associated with your historical data.

- **Email Address:** must be labeled Email Address
- **First Name:** label must match your attribute setup
- **Last Name:** label must match your attribute setup
- **Employee ID:** label must match your attribute setup
- **Status:** label must match your attribute setup

## Import users

Import your prepared User File to the Viva Glint People page to establish users and attributes for historical data.

> [!CAUTION]
> Avoid external, historical imports while Viva Glint surveys are live.

- [Import employee data](https://go.microsoft.com/fwlink/?linkid=2230742).
- Create a Distribution List with these historical employees. [Learn more](https://go.microsoft.com/fwlink/?linkid=2231414).
- Update the Distribution section of your survey program with your new Distribution List. [Learn more](https://go.microsoft.com/fwlink/?linkid=2231504).

## Import external data

To complete your external, historical import, access Viva Glint’s Advanced Configuration page. If you don't have access, confirm that:

- You are in the Company Admin User Role.
- The Advanced Configuration feature has been enabled for you as a user. [Learn more](https://go.microsoft.com/fwlink/?linkid=2240194).

> [!CAUTION]
> Your Glint survey program must be in an approved state while you import external, historical data and while reports generate. Ensure that your survey is approved before continuing.

To import historical users and their responses:

1. From your admin dashboard, select the **Configure** symbol, then in **Service Configuration** choose **Advanced Configuration**.
1. In the menu on the left, select **External Import**.
2. On the **External Import** page, make selections to import your data:
   1. **Manual Mode:** Leave this toggle switched to **Off**.
   1. **Survey Name:** Select your survey from the dropdown list.
   2. **Exception Date:** This field determines the start date displayed in reporting for this survey and must be **in the past** and **not overlap** with any scheduled surveys in this program.
   3. **Raw Score File:** Select **Choose File** and browse to select your **Raw Score File**.
   4. **New Distribution List Name:** Enter a name for a Distribution List that is used for historical import only and does not appear in your **Distribution List** page. Recommended: External-import-yyyymmdd.
   5. **User File:** Select **Choose File** and browse to select your **Respondent User File**.
   6. **Are you looking to append data to a survey cycle?:** Leave this toggle switched to **Off**.
   7. **Extra Options menu:** Leave collapsed, not applicable.
1. Select **Preview** and review the **Totals**, **Warnings**, and **Counts per Question** that appear.
:::image type="content" source="../../media/glint/setup/glint-ext-import-preview.png" alt-text="Image of import preview with warnings and counts":::
1. Confirm that:
   1. **Users in User File** matches the number of users in your **Respondent User File**.
   2. **Users in Score File** matches the number of users in your **Raw Score File**.
   3. **Score Users Missing in User File** is 0.
   4. **User File Users Not in Score File** matches the number of people who were invited but didn't respond to the survey.
   5. **Counts per Question**, when expanded, match the expected counts for each comment and response value.
1. After confirming the **Preview**, select **Save**.
2. Each section at the bottom of the page turns yellow as it processes and all turn green when the import is complete.

 :::image type="content" source="../../media/glint/setup/glint-ext-import-complete.png" alt-text="Image of successful external import":::

## Troubleshoot warnings and errors

If you encounter issues during your import, use this guidance to troubleshoot.

### Error at line 2: missing required field...

**Issue:** The .csv files uploaded to External Import aren't UTF-8 encoded, and are likely UTF-8 with BOM encoding.

**Resolution:** Resave files with UTF-8 encoding and reupload.

### User (email address) found in user file is NOT in client

**Issue:** The user email address for in your Respondent User File or Raw Score File doesn't match the email address for the user in the Viva Glint People page.

**Resolution:** Update the email address for the user(s) in Viva Glint to match the email address(es) in your files uploaded to Advanced Configuration External Import.

## Confirm expected results in your dashboard

After your External Import processes successfully in Viva Glint, go to your Dashboard and Reports to confirm that scores and data display as expected. Confirm that:

- Reporting hierarchies display as expected.
- Question sores are accurate.
- Respondent counts are accurate.
- Questions that exist in historical data and Viva Glint data trend as expected.
- Attributes and values that exist in historical data and Viva Glint data trend as expected.
- If comments were included, review the Comments report to confirm that counts are accurate.

> [!NOTE]
> Viva Glint’s Narrative Intelligence may take time to process large amounts of open-ended feedback. Revisit the Comments report after 24 hours if data is not fully populated.

   
