---
title: Manage apps in Microsoft Managed Desktop
description: Info about how to update line-of-business apps that are deployed to Microsoft Managed Desktop devices
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: tiaraquan
f1.keywords:
- NOCSH
ms.author: tiaraquan
manager: dougeby
ms.topic: article
ms.localizationpriority: medium
ms.date: 01/18/2019
ms.collection: M365-modern-desktop
---

# Manage line-of-business apps in Microsoft Managed Desktop

<!--Application management -->

There are a couple of ways to manage app updates, and deploy the updates to your Microsoft Managed Desktop devices. You can make app updates in Microsoft Managed Desktop admin center, or Intune.

<span id="update-app-mmd" />

## Update line-of-business apps in Microsoft Managed Desktop

**To update your line-of-business apps in Microsoft Managed Desktop admin center:**

1. Sign in to [Microsoft Managed Desktop admin center](https://aka.ms/mmdportal).
1. Under **Inventory**, select **Apps**.  
1. Select the app you want to updates, and then select **Edit**.
1. Under **Manage**, select **Properties**.
1. Select **App package file**, and then browse to upload a new app package file.
1. Select **App package file**.
1. Select the folder icon and browse to the location of your updated app file. Select **Open**. The app information is updated with the package information.
1. Verify that **App version** reflects the updated app package.

The updated app will be deployed to your user's devices.

<span id="update-app-intune" />

## Update line-of-business apps in Intune

**To update your line-of-business apps in Intune:**

1. Sign in to [Azure portal](https://portal.azure.com).
2. Select **All Services** > **Intune**. Intune is in the **Monitoring + Management** section.
3. Select **Client Apps > Apps**.
4. Find and select your app in the list of apps.
5. In the **Overview** section, select **Properties**.
6. Select **App package file**.
7. Select the folder icon and browse to the location of your updated app file. Select **Open**. The app information is updated with the package information.
8. Verify that **App version** reflects the updated app package.

<span id="roll-back-app-mmd" />

## Roll back an app to a previous version

When a new version of an app is deployed, and an error is found, you can roll back to a previous version. The process outlined below is for apps where the type is listed as **Windows MSI line-of-business app** or **Windows app (Win 32) - preview**

**To roll back a line-of-business app to a previous version:**

1. Sign in to [Microsoft Managed Desktop admin center](https://aka.ms/mmdportal).
2. Under **Inventory**, select **Apps**.  
3. Select the app you need to roll back, and then select **Edit**.
4. Under **Manage**, select **Properties**.
    - For **Windows MSI line-of-business app** apps, select **App information**, and then under **Ignore app version**, select **Yes**.
    - For **Windows app (Win 32) - preview** apps, select **App information**, select **Detection rules**, and then select **Add**.
    If there's an MSI rule, verify that **MSI product version check** is set to **No**.
5. [Upload a previous version of the app source file](../deploy/deploy-apps.md) to Microsoft Managed Desktop admin center.  
