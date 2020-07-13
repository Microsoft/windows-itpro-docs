---
title: Policy CSPs supported by HoloLens 2
description: Policy CSPs supported by HoloLens 2
ms.reviewer: 
manager: dansimp
ms.author: dansimp
ms.topic: article
ms.prod: w10
ms.technology: windows
author: manikadhiman
ms.localizationpriority: medium
ms.date: 05/11/2020
---

# Policy CSPs supported by HoloLens 2

> [!div class="op_single_selector"]
>
> - [HoloLens 2](policy-csps-supported-by-hololens2.md)
> - [HoloLens (1st gen) Commercial Suite](policy-csps-supported-by-hololens-1st-gen-commercial-suite.md)
> - [HoloLens (1st gen) Development Edition](policy-csps-supported-by-hololens-1st-gen-development-edition.md)
>

- [Accounts/AllowMicrosoftAccountConnection](policy-csp-accounts.md#accounts-allowmicrosoftaccountconnection)
- [ApplicationManagement/AllowAllTrustedApps](policy-csp-applicationmanagement.md#applicationmanagement-allowalltrustedapps)
- [ApplicationManagement/AllowAppStoreAutoUpdate](policy-csp-applicationmanagement.md#applicationmanagement-allowappstoreautoupdate)
- [ApplicationManagement/AllowDeveloperUnlock](policy-csp-applicationmanagement.md#applicationmanagement-allowdeveloperunlock)
- [Authentication/AllowFastReconnect](policy-csp-authentication.md#authentication-allowfastreconnect)
- [Authentication/PreferredAadTenantDomainName](policy-csp-authentication.md#authentication-preferredaadtenantdomainname)
- [Bluetooth/AllowDiscoverableMode](policy-csp-bluetooth.md#bluetooth-allowdiscoverablemode)
- [Bluetooth/LocalDeviceName](policy-csp-bluetooth.md#bluetooth-localdevicename)
- [Browser/AllowAutofill](policy-csp-browser.md#browser-allowautofill)
- [Browser/AllowCookies](policy-csp-browser.md#browser-allowcookies)
- [Browser/AllowDoNotTrack](policy-csp-browser.md#browser-allowdonottrack)
- [Browser/AllowPasswordManager](policy-csp-browser.md#browser-allowpasswordmanager)
- [Browser/AllowPopups](policy-csp-browser.md#browser-allowpopups)
- [Browser/AllowSearchSuggestionsinAddressBar](policy-csp-browser.md#browser-allowsearchsuggestionsinaddressbar)
- [Browser/AllowSmartScreen](policy-csp-browser.md#browser-allowsmartscreen)
- [Connectivity/AllowBluetooth](policy-csp-connectivity.md#connectivity-allowbluetooth)
- [Connectivity/AllowUSBConnection](policy-csp-connectivity.md#connectivity-allowusbconnection)
- [DeviceLock/AllowIdleReturnWithoutPassword](policy-csp-devicelock.md#devicelock-allowidlereturnwithoutpassword)
- [DeviceLock/AllowSimpleDevicePassword](policy-csp-devicelock.md#devicelock-allowsimpledevicepassword)
- [DeviceLock/AlphanumericDevicePasswordRequired](policy-csp-devicelock.md#devicelock-alphanumericdevicepasswordrequired)
- [DeviceLock/DevicePasswordEnabled](policy-csp-devicelock.md#devicelock-devicepasswordenabled)
- [DeviceLock/DevicePasswordExpiration](policy-csp-devicelock.md#devicelock-devicepasswordexpiration)
- [DeviceLock/DevicePasswordHistory](policy-csp-devicelock.md#devicelock-devicepasswordhistory)
- [DeviceLock/MaxDevicePasswordFailedAttempts](policy-csp-devicelock.md#devicelock-maxdevicepasswordfailedattempts)
- [DeviceLock/MaxInactivityTimeDeviceLock](policy-csp-devicelock.md#devicelock-maxinactivitytimedevicelock)
- [DeviceLock/MinDevicePasswordComplexCharacters](policy-csp-devicelock.md#devicelock-mindevicepasswordcomplexcharacters)
- [DeviceLock/MinDevicePasswordLength](policy-csp-devicelock.md#devicelock-mindevicepasswordlength)
- [Experience/AllowCortana](policy-csp-experience.md#experience-allowcortana)
- [Experience/AllowManualMDMUnenrollment](policy-csp-experience.md#experience-allowmanualmdmunenrollment)
- [Privacy/AllowInputPersonalization](policy-csp-privacy.md#privacy-allowinputpersonalization)
- [Privacy/LetAppsAccessAccountInfo](policy-csp-privacy.md#privacy-letappsaccessaccountinfo)
- [Privacy/LetAppsAccessAccountInfo_ForceAllowTheseApps](policy-csp-privacy.md#privacy-letappsaccessaccountinfo-forceallowtheseapps)
- [Privacy/LetAppsAccessAccountInfo_ForceDenyTheseApps](policy-csp-privacy.md#privacy-letappsaccessaccountinfo-forcedenytheseapps)
- [Privacy/LetAppsAccessAccountInfo_UserInControlOfTheseApps](policy-csp-privacy.md#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
- [Privacy/LetAppsAccessBackgroundSpatialPerception](policy-csp-privacy.md#privacy-letappsaccessbackgroundspatialperception)
- [Privacy/LetAppsAccessBackgroundSpatialPerception_ForceAllowTheseApps](policy-csp-privacy.md#privacy-letappsaccessbackgroundspatialperception-forceallowtheseapps)
- [Privacy/LetAppsAccessBackgroundSpatialPerception_ForceDenyTheseApps](policy-csp-privacy.md#privacy-letappsaccessbackgroundspatialperception-forcedenytheseapps)
- [Privacy/LetAppsAccessBackgroundSpatialPerception_UserInControlOfTheseApps](policy-csp-privacy.md#privacy-letappsaccessbackgroundspatialperception-userincontroloftheseapps)
- [Privacy/LetAppsAccessCamera_ForceAllowTheseApps](policy-csp-privacy.md#privacy-letappsaccesscamera-forceallowtheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessCamera_ForceDenyTheseApps](policy-csp-privacy.md#privacy-letappsaccesscamera-forcedenytheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessCamera_UserInControlOfTheseApps](policy-csp-privacy.md#privacy-letappsaccesscamera-userincontroloftheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessGazeInput](policy-csp-privacy.md#privacy-letappsaccessgazeinput) <sup>8</sup>
- [Privacy/LetAppsAccessGazeInput_ForceAllowTheseApps](policy-csp-privacy.md#privacy-letappsaccessgazeinput-forceallowtheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessGazeInput_ForceDenyTheseApps](policy-csp-privacy.md#privacy-letappsaccessgazeinput-forcedenytheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessGazeInput_UserInControlOfTheseApps](policy-csp-privacy.md#privacy-letappsaccessgazeinput-userincontroloftheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessCamera](policy-csp-privacy.md#privacy-letappsaccesscamera)
- [Privacy/LetAppsAccessLocation](policy-csp-privacy.md#privacy-letappsaccesslocation)
- [Privacy/LetAppsAccessMicrophone](policy-csp-privacy.md#privacy-letappsaccessmicrophone)
- [Privacy/LetAppsAccessMicrophone_ForceAllowTheseApps](policy-csp-privacy.md#privacy-letappsaccessmicrophone-forceallowtheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessMicrophone_ForceDenyTheseApps](policy-csp-privacy.md#privacy-letappsaccessmicrophone-forcedenytheseapps) <sup>8</sup>
- [Privacy/LetAppsAccessMicrophone_UserInControlOfTheseApps](policy-csp-privacy.md#privacy-letappsaccessmicrophone-userincontroloftheseapps) <sup>8</sup>
- [Search/AllowSearchToUseLocation](policy-csp-search.md#search-allowsearchtouselocation)
- [Security/RequireDeviceEncryption](policy-csp-security.md#security-requiredeviceencryption)
- [Settings/AllowDateTime](policy-csp-settings.md#settings-allowdatetime)
- [Settings/AllowVPN](policy-csp-settings.md#settings-allowvpn)
- [Speech/AllowSpeechModelUpdate](policy-csp-speech.md#speech-allowspeechmodelupdate)
- [System/AllowCommercialDataPipeline](policy-csp-system.md#system-allowcommercialdatapipeline)
- [System/AllowLocation](policy-csp-system.md#system-allowlocation)
- [System/AllowStorageCard](policy-csp-system.md#system-allowstoragecard)
- [System/AllowTelemetry](policy-csp-system.md#system-allowtelemetry)
- [Update/AllowAutoUpdate](policy-csp-update.md#update-allowautoupdate)
- [Update/AllowUpdateService](policy-csp-update.md#update-allowupdateservice)
- [Update/BranchReadinessLevel](policy-csp-update.md#update-branchreadinesslevel)
- [Update/DeferFeatureUpdatesPeriodInDays](policy-csp-update.md#update-deferfeatureupdatesperiodindays)
- [Update/DeferQualityUpdatesPeriodInDays](policy-csp-update.md#update-deferqualityupdatesperiodindays)
- [Update/ManagePreviewBuilds](policy-csp-update.md#update-managepreviewbuilds)
- [Update/PauseFeatureUpdates](policy-csp-update.md#update-pausefeatureupdates)
- [Update/PauseQualityUpdates](policy-csp-update.md#update-pausequalityupdates)
- [Update/ScheduledInstallDay](policy-csp-update.md#update-scheduledinstallday)
- [Update/ScheduledInstallTime](policy-csp-update.md#update-scheduledinstalltime)
- [Update/UpdateServiceUrl](policy-csp-update.md#update-updateserviceurl)
- [Wifi/AllowManualWiFiConfiguration](policy-csp-wifi.md#wifi-allowmanualwificonfiguration)
- [Wifi/AllowWiFi](policy-csp-wifi.md#wifi-allowwifi) <sup>8</sup>

Footnotes:

-   1 - Added in Windows 10, version 1607.
-   2 - Added in Windows 10, version 1703.
-   3 - Added in Windows 10, version 1709.
-   4 - Added in Windows 10, version 1803.
-   5 - Added in Windows 10, version 1809.
-   6 - Added in Windows 10, version 1903.
-   7 - Added in Windows 10, version 1909.
-   8 - Added in Windows 10, version 2004.

## Related topics

[Policy CSP](policy-configuration-service-provider.md)
