---
title: Create data import app
description: Learn how to create your application to transfer data from a source system to Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Create a data import app

Follow these steps to set up your console application:

Clone the app. Click on the green 'Clone' button on the top right. You can choose open with Visual Studio.
Create a new folder & select it for the clone to reside in when Visual Studio prompts.

If Visual Studio was open, close it. Open/re-open Visual Studio as admin.
On the right, click 'Open a local folder'. Choose the cloned folder.
At the top of Visual Studio, you will need to select a start up project. Select DescriptiveDataUploadApp.csproj.
Click the play button to 'Run' the app. Or, press Ctrl + F5.
A console should pop up asking you for inputs.
Values to enter in the console:
Note: None of the values require quotation marks ("") around them.
First, you will be asked for a client ID or app ID. This can be found in the registered app information on the Azure portal under Application (client) ID. If you are yet to create and register an app, follow this:

In the Azure portal, go to Azure Active Directory.
In the side bar, click on 'App registrations'.
Click on "+ New registration" on the top. Type in a name for the app and click 'Register'.
You should be able to grab the client/app ID from the overview page.
Second, you will be expected to enter the path to the zipped file. The format of the path expected is: C:\\Users\\JaneDoe\\OneDrive - Microsoft\\Desktop\\info.zip

Third, you will be expected to enter the Azure Active Directory tenant ID, which on app's overview page will appear as Directory (tenant) ID.

Lastly, you will need to enter the Certificate Name that is configured in your registered application.

Temporarily, we will be requiring the scale unit to be entered but this will be discontinued shortly. For the purpose of this project, you may input novaprdwus2-02.