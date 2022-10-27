---
ROBOTS: NOINDEX,NOFOLLOW
title: Changes to Viva Insights manager features
description: Learn what changes we're making to manager features
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: 
- m365initiative-viva-insights 
- viva-insights-leader
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin

---

# Upcoming changes to Viva Insights manager features

## Background

Viva Insights uses organizational data to determine the management hierarchy—also called the team reporting structure—that powers manager and leader insights. Features that use this data, along with resulting team structures, span the Viva Insights app in Teams and on the web, the Outlook add-in, and Viva Insights email features.

Today, Viva Insights gets organizational data from two sources: 

* **HR files uploaded by admins**. These files power organizational insights.
* **Azure Active Directory (AD)**. This data powers team insights, like:
    * Teamwork habits
    * Briefing email cards for managers
    * Digest email for managers

While end-users can modify the teams that result from Azure AD data, they can't modify the teams that result from HR files.

## What's changing?

Rather than using a data source for organization insights and another for team insights, Viva Insights will only use one: ***the HR file uploaded by the tenant admin***. Also, the product will no longer support end-user modifications to team members. Ending support for end-user-modified teams helps make sure there's only one organizational structure—that is, the one explicitly confirmed by the tenant admin.

## Why are we making these changes?

We're making these changes to keep a single, consistent organizational structure across Viva Insights features.

## How might these changes impact me?

You'll see different changes depending on whether you're a manager or non-manager.

* **If you're a manager** (that is, you have one or more people reporting directly to you in the company directory): 
    * Team member list: you're more likely to see a change if you've edited or confirmed your team member list for team insights. If you currently have a team member who doesn't report directly to you in your team member list, they'll stop appearing there.
    * Digest emails: team members you added to your list, but who don't report directly to you, won't appear on the **Catch up with your team** card anymore in the Briefing email. Team insights will no longer appear on digest Digest emails.
* **If you're a non-manager** (that is, you don't have anyone reporting directly to you in the company directory): 
    * Team member list: because we no longer support end-user modifications to the team member list, you'll lose access to team insights features. 
    * Briefing and Digest emails: team insights won't appear in your Digest email anymore, and you'll stop seeing the **Catch up with your Team** card in your daily Briefing email.

## When are these changes taking place?

We're expecting these updates to take place in late November 2022.

 
