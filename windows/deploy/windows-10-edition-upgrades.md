---
title: Windows 10 edition upgrade (Windows 10)
description: With Windows 10, you can quickly upgrade from one edition of Windows 10 to another, provided the upgrade path is supported.
ms.assetid: A7642E90-A3E7-4A25-8044-C4E402DC462A
ms.prod: w10
ms.mktglfcycl: deploy
localizationpriority: high
ms.sitesec: library
ms.pagetype: mobile
author: greg-lindsay
---

# Windows 10 edition upgrade
**Applies to**

-   Windows 10
-   Windows 10 Mobile

With Windows 10, you can quickly upgrade from one edition of Windows 10 to another, provided the upgrade path is supported. For information on what edition of Windows 10 is right for you, see [Compare Windows 10 Editions](https://go.microsoft.com/fwlink/p/?LinkID=690882). For a comprehensive list of all possible upgrade paths to Windows 10, see [Windows 10 upgrade paths](windows-10-upgrade-paths.md).

The following table shows the methods and paths available to change the edition of Windows 10 that is running on your computer. **Note**: The reboot requirement for upgrading from Pro to Enterprise was removed in version 1607. 

X = unsupported <BR>
✔ (green) = supported; reboot required<BR>
✔ (blue) = supported; no reboot required. 


|Method |Home > Pro |Home > Education |Pro > Education |Pro > Enterprise |Ent > Education |Mobile > Mobile Enterprise |
|-------|-----------|-----------------|----------------|-----------------|----------------|--------|
| Using mobile device management (MDM) |![unsupported](images/x_blk.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_blu.png) |![supported](images/check_grn.png) |![supported](images/check_blu.png) |
| Using a provisioning package |![unsupported](images/x_blk.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_blu.png) |
| Using a command-line tool |![unsupported](images/x_blk.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_blu.png) |![supported](images/check_grn.png) |![unsupported](images/x_blk.png) |
| Entering a product key manually |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_grn.png) |![supported](images/check_blu.png) |![supported](images/check_grn.png) |![unsupported](images/x_blk.png) |
| Purchasing a license from the Windows Store |![supported](images/check_grn.png) |![unsupported](images/x_blk.png) |![unsupported](images/x_blk.png) |![unsupported](images/x_blk.png) |![unsupported](images/x_blk.png) |![unsupported](images/x_blk.png) |

>**Note**: Each desktop edition in the table also has an N and KN edition. These editions have had media-related functionality removed. Devices with N or KN editions installed can be upgraded to corresponding N or KN editions using the same methods.

## Upgrade using mobile device management (MDM)
- To upgrade desktop editions of Windows 10 using MDM, you'll need to enter the product key for the upgraded edition in the **UpgradeEditionWithProductKey** policy setting of the **WindowsLicensing** CSP. For more info, see [WindowsLicensing CSP](https://go.microsoft.com/fwlink/p/?LinkID=690907).

- To upgrade mobile editions of Windows 10 using MDM, you'll need to enter the product key for the upgraded edition in the **UpgradeEditionWithLicense** policy setting of the **WindowsLicensing** CSP. For more info, see [WindowsLicensing CSP](https://go.microsoft.com/fwlink/p/?LinkID=690907).

## Upgrade using a provisioning package
Download Windows Configuration Designer from the Windows Store.

- To use Windows Configuration Designer to create a provisioning package for upgrading desktop editions of Windows 10, go to **Runtime settings &gt; EditionUpgrade &gt; UpgradeEditionWithProductKey** in the **Available customizations** panel in Windows Configuration Designer and enter the product key for the upgraded edition.

- To use Windows Configuration Designer to create a provisioning package for upgrading mobile editions of Windows 10, go to **Runtime settings &gt; EditionUpgrade &gt; UpgradeEditionWithLicense** in the **Available customizations** panel in Windows Configuration Designer and enter the product key for the upgraded edition.

For more info on creating and applying a provisioning package using Windows ICD, see [Build and apply a provisioning package](https://go.microsoft.com/fwlink/p/?LinkID=533700).

## Upgrade using a command-line tool
You can run the changepk.exe command-line tool to upgrade devices to a supported edition of Windows 10:

`changepk.exe /ProductKey <enter your new product key here>`

## Upgrade by manually entering a product key
If you are upgrading only a few devices, you may want to enter a product key for the upgraded edition manually.

**To manually enter a product key**

1.  From either the Start menu or the Start screen, type 'Activation' and click on the Activation shortcut.

2.  Click **Change product key**.

3.  Enter your product key.

4.  Follow the on-screen instructions.

## Upgrade by purchasing a license from the Windows Store
If you do not have a product key, you can upgrade your edition of Windows 10 through the Windows Store.

**To upgrade through the Windows Store**

1.  From either the **Start** menu or the **Start** screen, type 'Activation' and click on the Activation shortcut.

2.  Click **Go to Store**.

3.  Follow the on-screen instructions.
    
    **Note**<br>If you are a Windows 10 Home N or Windows 10 Home KN user and have trouble finding your applicable upgrade in the Windows Store, click [here](ms-windows-store://windowsupgrade/).

 

 

 





