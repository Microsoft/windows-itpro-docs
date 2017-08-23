---
title: Assign devices to servicing channels for Windows 10 updates (Windows 10)
description: tbd
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
author: DaniHalfin
ms.localizationpriority: high
ms.author: daniha
ms.date: 07/27/2017
---

# Assign devices to servicing channels for Windows 10 updates


**Applies to**

- Windows 10
- Windows 10 Mobile

> **Looking for consumer information?** See [Windows Update: FAQ](https://support.microsoft.com/help/12373/windows-update-faq) 

>[!TIP]
>If you're not familiar with the Windows 10 servicing or release channels, read [Servicing Channels](waas-overview.md#servicing-channels) first.
>
>Due to [naming changes](waas-overview.md#naming-changes), older terms like CB,CBB and LTSB may still be displayed in some of our products.

Semi-Annual Channel (Targeted) is the default servicing channel for all Windows 10 devices except those with the LTSB edition installed. The following table shows the servicing channels available to each edition of Windows 10. 

| Windows 10 edition | Semi-Annual Channel (Targeted) | Semi-Annual Channel | Long-Term Servicing Channel | Insider Program |
| --- | --- | --- | --- | --- |
| Home | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Pro | ![yes](images/checkmark.png) | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Enterprise | ![yes](images/checkmark.png) | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Enterprise LTSB | ![no](images/crossmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) | ![no](images/crossmark.png) |
| Pro Education | ![yes](images/checkmark.png) | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Education | ![yes](images/checkmark.png) | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Mobile | ![yes](images/checkmark.png) | ![no](images/crossmark.png) | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |
| Mobile Enterprise | ![yes](images/checkmark.png) | ![yes](images/checkmark.png)  | ![no](images/crossmark.png) | ![yes](images/checkmark.png) |



>[!NOTE]
>The LTSB edition of Windows 10 is only available through the [Microsoft Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx).

## Assign devices to Semi-Annual Channel

>[!IMPORTANT]
>Due to [naming changes](waas-overview.md#naming-changes), older terms like CB,CBB and LTSB may still be displayed in some of our products.
>
>In the following settings CB refers to Semi-Annual Channel (Targeted), while CBB refers to Semi-Annual Channel.

**To assign a single PC locally to CBB**

1. Go to **Settings** > **Update & security** > **Windows Update** > **Advanced options**.
2. Select **Defer feature updates**.

**To assign PCs to CBB using Group Policy**

- In Windows 10, version 1511:

    Computer Configuration > Administrative Templates > Windows Components > Windows Update > **Defer Upgrades and Updates**

- In Windows 10, version 1607:

    Computer Configuration > Administrative Templates > Windows Components > Windows Update > Defer Windows Updates > **Select when Feature Updates are received** - enable policy and set branch readiness level to CBB
    
**To assign PCs to CBB using MDM**

- In Windows 10, version 1511:

    ../Vendor/MSFT/Policy/Config/Update/**RequireDeferUpgrade**

- In Windows 10, version 1607:

    ../Vendor/MSFT/Policy/Config/Update/**BranchReadinessLevel**
    
**To assign Windows 10 Mobile Enterprise to CBB using MDM**

- In Windows 10 Mobile Enterprise, version 1511:

    ../Vendor/MSFT/Policy/Config/Update/RequireDeferUpgrade

- In Windows 10 Mobile Enterprise, version 1607:

    ../Vendor/MSFT/Policy/Config/Update/BranchReadinessLevel

## Enroll devices in the Windows Insider Program

Enrolling devices in the Windows Insider Program is simple and requires only a Microsoft account. To enroll a device in the Windows Insider Program, complete the following steps on the device that you want to enroll: 

1. Go to **Start** > **Settings** > **Update & security** > **Windows Insider Program**.

2. Select **Get started**.  
    >[!NOTE]
    >If you didn’t use a Microsoft account to log in to the computer, you’ll be prompted to log in. If you don’t have a Microsoft account, you can create one now. 
    
3. Read the privacy statement and program terms, and then click **Next**.

6.	Click **Confirm**, and then select a time to restart the computer.

## Install your first preview build from the Windows Insider Program

After enrolling your devices, you are ready to install your first preview build. To do so, go to **Start** > **Settings** > **Update & security** > **Windows Insider Program** to select your Insider level. The device receives the most recent Windows Insider build for the Insider level you select. 

The options for Insider level are:
- **Release Preview**: Insiders on this level receive builds of Windows just before Microsoft releases them for Semi-Annual Channel. Although these builds aren’t final, they are the most complete and stable builds available to Windows Insider Program participants. This level provides the best testing platform for organizations that conduct early application compatibility testing on Windows Insider PCs.
- **Slow**: The Slow Windows Insider level is for users who enjoy seeing new builds of Windows with minimal risk to their devices but still want to provide feedback to Microsoft about their experience with the new build.
- **Fast**: This level is best for Insiders who would like to be the first to experience new builds of Windows, participate in identifying and reporting issues to Microsoft, and provide suggestions on new functionality. 

>[!NOTE]
>Once your machine is updated to Windows 10 and you select your desired flight ring, the process known as "Compatibility check" will need to run in the background. There is no manual way to force this process to run. This process allows for the discovery of your OS type (32-bit, 64-bit), build edition (Home, Pro, Enterprise), country and language settings, and other required information. Once this process is complete, your machine will be auto-targeted for the next available flight for your selected ring. For the first build on any given machine, this may take up to 24 hours to complete.

## Block access to Windows Insider Program

To prevent devices in your enterprise from being enrolled in the Insider Program for early releases of Windows 10:

- Group Policy: Computer Configuration\Administrative Templates\Windows Components\Data Collection and Preview Builds\\**Toggle user control over Insider builds**
- MDM: Policy CSP - [System/AllowBuildPreview](https://msdn.microsoft.com/library/windows/hardware/dn904962%28v=vs.85%29.aspx#System_AllowBuildPreview)

## Switching channels

During the life of a device, it may be necessary or desirable to switch between the available channels. Depending on the channel you are using, the exact mechanism for doing this can be different; some will be simple, others more involved.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">From this channel</th>
<th align="left">To this channel</th>
<th align="left">You need to</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left" rowspan="3">Windows Insider Program</td>
<td align="left">Semi-Annual Channel (Targeted)</td>
<td align="left">Wait for the final Semi-Annual Channel release.</td>
</tr>
<tr class="even">
<td align="left">Semi-Annual Channel</td>
<td align="left">Not directly possible, because Windows Insider Program devices are automatically upgraded to the Semi-Annual Channel (Targeted) release at the end of the development cycle.</td>
</tr>
<tr class="odd">
<td align="left">Long-Term Servicing Channel</td>
<td align="left">Not directly possible (requires wipe-and-load).</td>
</tr>
<tr class="even">
<td align="left" rowspan="3">Semi-Annual Channel (Targeted)</td>
<td align="left">Insider</td>
<td align="left">Use the Settings app to enroll the device in the Windows Insider Program.</td>
</tr>
<tr class="odd">
<td align="left">Semi-Annual Channel</td>
<td align="left">Select the <strong>Defer upgrade</strong> setting, or move the PC to a target group or flight that will not receive the next upgrade until it is business ready. Note that this change will not have any immediate impact; it only prevents the installation of the next Semi-Annual Channel release.</td>
</tr>
<tr class="even">
<td align="left">Long-Term Servicing Channel</td>
<td align="left">Not directly possible (requires wipe-and-load).</td>
</tr>
<tr class="odd">
<td align="left" rowspan="3">Semi-Annual Channel</td>
<td align="left">Insider</td>
<td align="left">Use the Settings app to enroll the device in the Windows Insider Program.</td>
</tr>
<tr class="even">
<td align="left">Semi-Annual Channel (Targeted)</td>
<td align="left">Disable the <strong>Defer upgrade</strong> setting, or move the device to a target group or flight that will receive the latest Current Semi-Annual Channel release.</td>
</tr>
<tr class="odd">
<td align="left">Long-Term Servicing Channel</td>
<td align="left">Not directly possible (requires wipe-and-load).</td>
</tr>
<tr class="even">
<td align="left" rowspan="3">Long-Term Servicing Channel</td>
<td align="left">Insider</td>
<td align="left">Use media to upgrade to the latest Windows Insider Program build.</td>
</tr>
<tr class="odd">
<td align="left">Semi-Annual Channel (Targeted)</td>
<td align="left">Use media to upgrade to a later Semi-Annual Channel build. (Note that the Semi-Annual Channel build must be a later build.)</td>
</tr>
<tr class="even">
<td align="left">Semi-Annual Channel</td>
<td align="left">Use media to upgrade to a later Semi-Annual Channel for Business build (Semi-Annual Channel build plus fixes). Note that it must be a later build.</td>
</tr>
</tbody>
</table>

## Block user access to Windows Update settings

In Windows 10, administrators can control user access to Windows Update.
By enabling the Group Policy setting under **Computer Configuration\Administrative Templates\Windows Components\Windows update\Remove access to use all Windows update features**, administrators can disable the "Check for updates" option for users. Any background update scans, downloads and installations will continue to work as configured.

>[!NOTE]
> In Windows 10, any Group Policy user configuration settings for Windows Update were deprecated and are no longer supported on this platform.

## Steps to manage updates for Windows 10

| | |
| --- | --- |
| ![done](images/checklistdone.png) | [Learn about updates and servicing channels](waas-overview.md) |
| ![done](images/checklistdone.png) | [Prepare servicing strategy for Windows 10 updates](waas-servicing-strategy-windows-10-updates.md) |
| ![done](images/checklistdone.png) | [Build deployment rings for Windows 10 updates](waas-deployment-rings-windows-10-updates.md) |
| ![done](images/checklistdone.png) | Assign devices to servicing channels for Windows 10 updates (this topic) |
| ![to do](images/checklistbox.gif) | [Optimize update delivery for Windows 10 updates](waas-optimize-windows-10-updates.md) |
| ![to do](images/checklistbox.gif) | [Deploy updates using Windows Update for Business](waas-manage-updates-wufb.md)</br>or [Deploy Windows 10 updates using Windows Server Update Services](waas-manage-updates-wsus.md)</br>or [Deploy Windows 10 updates using System Center Configuration Manager](waas-manage-updates-configuration-manager.md) |

## Related topics

- [Update Windows 10 in the enterprise](index.md)
- [Deploy updates for Windows 10 Mobile Enterprise and Windows 10 IoT Mobile](waas-mobile-updates.md) 
- [Configure Delivery Optimization for Windows 10 updates](waas-delivery-optimization.md)
- [Configure BranchCache for Windows 10 updates](waas-branchcache.md)
- [Configure Windows Update for Business](waas-configure-wufb.md)
- [Integrate Windows Update for Business with management solutions](waas-integrate-wufb.md)
- [Walkthrough: use Group Policy to configure Windows Update for Business](waas-wufb-group-policy.md)
- [Walkthrough: use Intune to configure Windows Update for Business](waas-wufb-intune.md)
- [Manage device restarts after updates](waas-restart.md)


