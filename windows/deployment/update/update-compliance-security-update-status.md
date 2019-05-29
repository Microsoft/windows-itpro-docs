---
title: Update Compliance - Security Update Status report
description: an overview of the Security Update Status report
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: deploy
author: Jaimeo
ms.author: jaimeo
ms.collection: M365-analytics
ms.topic: article
---

# Security Update Status

![The Security Update Status report](images/UC_workspace_SU_status.png)

The Security Update Status section provides information about [security updates](waas-quick-start.md#definitions) across all devices. The section tile within the [Overview Blade](update-compliance-using.md#overview-blade) lists the percentage of devices on the latest security update available. Meanwhile, the blades within show the percentage of devices on the latest security update for each Windows 10 version and the deployment progress toward the latest two security updates.  

The **Overall Security Update Status** blade provides a visualization of devices that are and do not have the latest security updates. Below the visualization are all devices further broken down by operating system version and a count of devices that are up to date and not up to date. The **Not up to date** column also provides a count of update failures.
 
The **Latest Security Update Status** and **Previous Security Update Status** tiles are stacked to form one blade. The **Latest Security Update Status** provides a visualization of the different deployment states devices are in regarding the latest update for each build (or version) of Windows 10, along with the revision of that update. The **Previous Security Update Status** blade provides the same information without the accompanying visualization. 

The deployment and detailed states of an update, are described as follows:

**Deployment States**
* **Unknown**: Indicates a device that has not been scanned for an update for some time.
* **In Progress**: Indicates that an update is currently being applied to a specific device.
* **Progress Stalled**: Indicates that an update has stopped for some reason, such as network failure.
* **Failed**: Indicates that the update process for a specific device has not been successful.
* **Update Completed**: Indicates that a device has been updated successfully.
* **Deferred**: Indicates that an update has been postponed to a later time. 
* **Cancelled**: Indicates that an update has been cancelled by the user.

**Detailed States**
* **Download Started**: Indicates that a specific update has started to download.
* **Download Succeeded**: Indicates that the download of a specific update has been successful.
* **Download Hand Off**: Indicates that you can continue downloading an update at the point where it was stopped.
* **Install Hand Off**: Indicates that you can continue installing an update at the point where it was stopped.
* **Reboot Pending**: Indicates that you need reboot the device to complete the update process.
* **Service Stack Downloaded:** Indicates that the Service Stack Update (The component that installs Windows update) is downloading.
* **Update Offered:** Indicates that an update is offered, being optional the application of the same.
* **Update Detected:** Indicates that a needed update is detected to apply.
 
The various deployment states reported by devices are as follows:
* **Installed** devices are devices that have completed installation for the given update.
* When a device is counted as **In Progress or Deferred**, it has either begun the installation process for the given update or has been intentionally deferred or paused using Windows Update for Business Settings.
* Devices that have **Update Issues** have failed to update at some point during the installation process of the given security update or have not seen progress for a period of seven days.
* If a device should be, in some way, progressing toward this security update, but its status cannot be inferred, it will count as **Status Unknown**. This is most often devices that have not scanned for an update in some time, or devices not being managed through Windows Update.

The rows of each tile in this section are interactive; selecting them will navigate you to the query that is representative of that row and section. 
