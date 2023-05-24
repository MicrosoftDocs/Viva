---
title: Manage language translations in Viva Glint programs 
description: "Survey content and email communications should be sent to employees in their preferred language. Managing language translations is easy within Viva Glint program."
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva-goals
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high pri
ms.date: 04/28/2023
---

# Manage language translations in Viva Glint programs 

English is the default language for all Microsoft Viva Glint programs, but surveys and email communications should be sent to employees in their preferred language. Viva Glint provides customers with more than 70 language translation for standard program content. Language translations are set during the initial survey configuration or added later as needed. Exporting a file that includes the default language and all relevant translations allows reviewing, adding, or editing translations to happen in one place. 

Translations may be needed for email communications and survey content such as single-item questions, statements, multiple-choice questions, rating labels, and text snippets.  

There are four steps for making language translations: 

1. Export content from the Viva Glint program into a *.csv* or *.xlsx* file 
2. Translate content 
3. Review translations 
4. Import content back into the Viva Glint program 

## Export survey and email text 

Follow these steps: 

1. Navigate to the appropriate survey program. 
2. From the Actions dropdown menu and select **Export Program Content**. 
3. Choose if you will export email content, survey content, or both.  
4. Select the languages you would like to export from the Languages to include section. Default text will already be included in addition to whatever additional languages are chosen. 
5. Select **Generate CSV**. 
6. From the file generated, make translations to import back into Viva Glint. 

>[!NOTE]
> The email content will be downloaded as its own separate Excel document. Survey content will download as a zip file with one file containing survey questions and text snippets.

>[!NOTE]
> The Viva Glint system requires that one language document is initially exported and then later imported back into the program before the process can be repeated for other languages.

## Make language edits 

The additional language column in your file must match exactly the default language column. If not, it must be corrected for accuracy as this is directly placed into emails and survey content.  

>[!CAUTION]
> Macros should never be translated nor deleted.

### Make language edits to survey emails and items 

Export one language initially, make the translations and add them to the appropriate file column.  

### Make language edits to survey questions (items) from the Question Library 

If you are using Glint standard survey items, translations are already available in 70+ languages and unless questions are edited (customized), this process is unnecessary. 

To make language translations or edits for items in the Question Library: 

1. From the Question Library filter the questions for export. 
2. Select **Export Questions** from the *Actions* dropdown menu. 
3. Choose the language(s) to include from the search box in the *Choose Which Language to Export window*. 
4. Select your export format. 
5. Select **Export**. A message displays indicating that your file is being downloaded. 
6. After the report is downloaded, select **Close Window**. 

### Making language edits to text snippets 

Text snippets include instructional text and navigational prompts. The focus should be on the survey intro and demo text. Each item translated must match exactly the exported item. 

## Import translated content and emails back to Viva Glint 

After all changes have been made and the files are ready to send back, follow these steps: 

1. Select the appropriate survey program and from the Actions dropdown menu, select **Import Program Content**. 
2. Follow the onscreen prompts to **Import Email Content** or **Import Survey Content**. 
3. Documents can be uploaded individually or combined into a zip file and imported in bulk. 
4. Approve the survey and the edited translations are added to your survey. 

At this point, you can export the remainder of your survey emails in bulk across other languages and make the needed edits. 

### Import translated items to the Question Library 

Back on the Question Library page, select **Import Questions** from the *Actions* dropdown menu. 

1. Drag and drop or browse to find the translated file and place it in the box for uploading. 
2. Select **Next**. 
3. If everything looks as expected, select **Make Changes**.

## Translation tips for exported items 

From the file that has been generated, use a translator to make exact changes to the approved default text.  

**Do’s:** 

- Keep the translated content in the same cell and columns. 
- Ensure that there are no spaces added before/after the updated content. Ensure there is also consistent punctuation at the end of sentences (that is, all using a period or none using a period). 
- Check for grammatical errors. 

**Don’ts:** 

- Don’t edit, translate, or delete any bracketed text. Do not edit macros.  
- Don’t make visual, formatting, or other stylistic changes unless it improves clarity. Changes should never alter the meaning conveyed in the original English text. 
- Don’t add personal comments. ` 
- Don’t add new or additional columns or remove columns.  

## Reviewer tips for translated items 

A second person should be called upon to review the translated items. Translated text will appear exactly as it is returned to Viva Glint so ensure its accuracy. 

**Do’s:** 

- Focus on copy-editing by fixing any typographical or grammatical errors. 
- Confirm that the original meaning of the question remains intact. 
- Keep translated content in the same cell and columns. 

**Don’ts:** 

- Don’t rewrite entire sentences. 
- Don’t move translated content to different cells or columns. 
- Don’t add personal comments. 

## Include language codes in your Employee Attribute File 

In order for your people to receive surveys and email communications in their preferred language, the language code must be part of each individual’s Employee Attribute File. 

The following language codes must be used: 

|**Language**| **Language Code**|
|-----------|-----------|
|English (US) | en_US |
|Afrikaans  | af_ZA |
|Albanian   | af_ZA |
|Arabic  | af_ZA |
|Austrian (German) | de_AT  |
|Bengali | bn_BD  |
|Bosnian  | bs_BA |
|Bulgarian  | bg_BG  |
|Burmese  | my_MM   |
|Chinese (Hong Kong)  | zh_HK  |
|Chinese (Simplified)  | zh_CN  |
|Chinese (Traditional)  | zh_TW  |
|Croatian  | hr_HR |
|Czech   | cs_CZ |
|Danish   | da_DK  |
|Dutch   | nl_NL   |
|English (UK)    | en_GB   |
|Estonian   | et_EE   |
|Finnish    | fi_FI   |
|French    | fr_FR   |
|French (Canadian)    | fr_CA   |
|Georgian    | ka_GE   |
|German     | de_DE    |
|Greek     | el_GR    |
|Gujarati     | gu_IN    |
|Haitian Creole    | fr_HT    |
|Hebrew      |he_IL    |
|Hindi      |hi_IN    |
|Hungarian      |hu_HU    |
|Hungarian      |hu_HU    |