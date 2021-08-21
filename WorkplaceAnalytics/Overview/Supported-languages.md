---

title: Workplace Analytics language support and guidelines
description: Describes the privacy and data access controls available in Workplace Analytics 
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin

---

# Workplace Analytics language support and guidelines

The Workplace Analytics user interface is currently available in Chinese (Simplified), Chinese (Traditional), French (France), German (Germany), Italian (Italy), Japanese, Korean, Portuguese (Brazil), Russian (Russia), Spanish (Spain), and English (United States).

The Workplace Analytics user interface automatically uses your locale (language and region) setting, as specified in one of the following sources:

* Windows
* your web browser
* the locale that is set for your Exchange Online mailbox

You can override this setting. To do so, edit the URL that you use to access Workplace Analytics.

* In the URL, replace the locale identifier (for example, "en-us" for US English) with a different locale identifier. The table under [Supported locales](#supported-locales) lists all of the supported locale identifiers for Workplace Analytics.

    For example, replace /en-us/ in the following URL:

    https://workplaceanalytics.office.com/en-us/ 

    with /ja-jp/, to indicate Japanese:

    https://workplaceanalytics.office.com/ja-jp/ 

#### Supported locales

Language and region | Locale identifier
------ | ------
Chinese (Simplified) | zh-cn
Chinese (Traditional) | zh-tw
French (France) | fr-fr
German (Germany) | de-de
Italian (Italy) | it-it
Japanese | ja-jp
Korean | ko-kr
Portuguese (Brazil) | pt-br
Russian (Russia) | ru-ru
Spanish (Spain) | es-es
English (United States) | en-us

### Use of non-English data

In certain circumstances, you can use Workplace Analytics with _data_ that is in other languages. Follow these guidelines:

* Query names and descriptions must be in English, Japanese, or French.

   ![Query names and descriptions.](../Images/WpA/Overview/query-name-description.png)

* Column headers for the organizational data when you [prepare the organizational data](../Setup/Prepare-organizational-data.md) must be in English.

* When an analyst selects metrics while building a [query](../tutorials/query-basics.md), the metric names they choose can be in the language of their choice. See [Supported languages for column headers](../use/view-download-and-export-query-results.md?branch=pas-pd-other-char-sets#supported-languages-for-column-headers).

* For content within organizational data, you can use languages other than English.

## Privacy settings

In [Privacy settings](../use/privacy-settings.md), when adding the subject line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in other languages such as Japanese or Chinese. For best results, use single words, separated by a semicolon.

![Exclude terms from subject line.](../Images/WpA/Overview/exclude-terms-from-subject-line.png)

We appreciate all your feedback. To report any language-related issues, use the **Send feedback** button.

### Related topics

* [Supported languages in meeting exclusion rules](../tutorials/meeting-exclusion-concept.md#supported-languages)
* [Settings](../use/settings.md)
* [Privacy settings considerations for Workplace Analytics](../Privacy/privacy-considerations.md)
