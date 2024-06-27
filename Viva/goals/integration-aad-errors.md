---
ms.date: 06/27/2024
title: Troubleshoot AAD errors for integrations
ms.reviewer: 
ms.author: v-nstockwell
author: DefinitelyNotNitza
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn about different kinds of AAD errors and how to resolve them."
---

# Troubleshoot AAD errors for integrations

## Different kinds of AAD errors

If you encounter an AAD invalid grant error for an integration, it is likely that you've run into one of these common error types based on the configuration of your account or device.

### AADSTS530003: Your device is required to be managed to access this resource

The device on which this connection was first created might not have been in a managed state. Try re-authenticating or creating a new connection.

### AADSTS530002: Your device is required to be compliant to access this resource  

The device on which this connection was first created is no longer in a compliant state. Try re-authenticating or creating a new connection.

### AADSTS53000: Device is not in required device state: compliant. Conditional Access policy requires a compliant device, and the device is not compliant. The user must enroll their device with an approved MDM provider like Intune

The device on which this connection was first created is no longer in a compliant state. Try re-authenticating or creating a new connection.

### AADSTS50173: The provided grant has expired due to it being revoked, a fresh auth token is needed. The user might have changed or reset their password

The current token being used for this connection has expired. Try re-authenticating or creating a new connection.

### AADSTS50076: Due to a configuration change made by your administrator, or because you moved to a new location, you must use multi-factor authentication to access

Authentication failed. Try re-authenticating or creating a new connection.

### AADSTS500341: The user account &lt;account ID&gt; has been deleted from the &lt;AAD&gt; directory. To sign into this application, the account must be added to the directory

The user account with which this connection was first created is no longer in an active state. Try creating a new connection.

### AADSTS50034: The user account &lt;account ID&gt; does not exist in the &lt;AAD&gt; directory. To sign into this application, the account must be added to the directory

The user account with which this connection was first created is no longer in an active state. Try creating a new connection.

### AADSTS135011: Device used during the authentication is disabled

The device on which this connection was first created is disabled. Try re-authenticating or creating a new connection.

### AADSTS700082: The refresh token has expired due to inactivity. The token was issued on &lt;time stamp&gt; and was inactive for &lt;duration in days&gt;

The current token being used for this connection has expired. Try re-authenticating or creating a new connection.

### AADSTS135010: UserPrincipal doesn't have the key ID configured

Try re-authenticating or creating a new connection.

## Frequently asked questions

### How do I re-authenticate a connection?

If you are the owner of the errored-out connection, you will see the **Try again** option in the integration popover. Select **Try again** to trigger re-authentication.

:::image type="content" source="../media/goals/integration-aad-errors/try-again.png" alt-text="Screenshot of the ADO automatic progress update dialogue showing a failure to authenticate and the Try again option." lightbox="../media/goals/integration-aad-errors/try-again.png":::

:::image type="content" source="../media/goals/integration-aad-errors/reauth-ado-connection.png" alt-text="Screenshot showing the Re-authenticate Azure DevOps connection dialog." lightbox="../media/goals/integration-aad-errors/reauth-ado-connection.png":::

The connection can also be re-authenticated by navigating to **Account Settings** > **Preferences** > **My integrations** and re-authenticating the connection with the associated error.

:::image type="content" source="../media/goals/integration-aad-errors/ado-config.png" alt-text="Screenshot showing the Azure DevOps Configuration settings with an emphasis on the Re-authenticate column." lightbox="../media/goals/integration-aad-errors/ado-config.png":::

If the error still appears, try creating a new connection from the integration connection dropdown at the top of the integration setup page.

:::image type="content" source="../media/goals/integration-aad-errors/connect-to-ado.png" alt-text="Screenshot showing the Connect to Azure DevOps dialog with an emphasis on the connection name, connection search box, and option to add a new connection." lightbox="../media/goals/integration-aad-errors/connect-to-ado.png":::

If you do not own the errored-out connection and are instead sharing a connection owned by another user, you can either create a new connection as shown above or reach out to your Viva Goals administrator for help.

If you are a Viva Goals administrator, you can re-authenticate the existing connection or create a new connection by navigating to **Admin** > **Integrations** > **Specific integration** and selecting **Manage**. There, you will see a list of your organization's connections and can choose whichever one you need.

:::image type="content" source="../media/goals/integration-aad-errors/ado-config-admin.png" alt-text="Screenshot showing the Azure DevOps configuration settings, with an emphasis on the New Connection button and the Re-authenticate and Edit columns." lightbox="../media/goals/integration-aad-errors/ado-config-admin.png":::

### How do I create a new connection?

To set up a connection, select **Enable** on the integration you want to set up a connection for, then follow the setup steps. Remember: only admins or connection owners can edit connections.

To make connections public (that is, usable by everyone in the organization) or private, toggle the **Share connection** checkbox. Users will be able to see their private connections, followed by their public connections (if any).

If you are a Viva Goals administrator or a tenant administrator, you can create a new connection by navigating to **Admin** > **Integrations** in the Viva Goals web or Teams app, selecting **Manage** for the appropriate integration, and finally selecting **New Connection**. You can also re-authenticate the connection from this page if needed.

If you do not have admin access, you can create a new connection in two ways:

- On the integration setup page, select **Add new connection** on the connection dropdown.
    :::image type="content" source="../media/goals/integration-aad-errors/connect-to-ado.png" alt-text="Screenshot showing the Connect to Azure DevOps dialog with an emphasis on the connection name, connection search box, and option to add a new connection." lightbox="../media/goals/integration-aad-errors/connect-to-ado.png":::
- Navigate to **Account Settings** > **Preferences** > **My integrations** and add a new connection.
    :::image type="content" source="../media/goals/integration-aad-errors/ado-config-nc.png" alt-text="Screenshot showing the Azure DevOps Configuration settings with an emphasis on the New Connection button." lightbox="../media/goals/integration-aad-errors/ado-config-nc.png":::

### How do I replace the old errored-out connection with a new connection in the integrated key result or initiative?

When you see the option to "edit integration," you can simply select **Edit** to navigate to the integration setup page, then choose the new connection from the connection dropdown on the top. Once the new connection has been chosen, select the necessary details in integration setup and save to resume automatic progress updates.

If you don't have the option to "edit integration," you can either reach out to the key result/initiative owner or a Viva Goals administrator to help update the connection and resume automatic progress updates.
