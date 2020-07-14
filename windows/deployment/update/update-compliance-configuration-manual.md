---
title: Manually configuring devices for Update Compliance
ms.reviewer: 
manager: laurawi
description: Manually configuring devices for Update Compliance
keywords: update compliance, oms, operations management suite, prerequisites, requirements, updates, upgrades, antivirus, antimalware, signature, log analytics, wdav
ms.prod: w10
ms.mktglfcycl: deploy
ms.pagetype: deploy
audience: itpro
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: medium
ms.collection: M365-analytics
ms.topic: article
---

# Manually Configuring Devices for Update Compliance

There are a number of requirements to consider when manually configuring Update Compliance. These can potentially change with newer versions of Windows 10. The [Update Compliance Configuration Script](update-compliance-configuration-script.md) will be updated when any configuration requirements change so only a redeployment of the script will be required.

The requirements are separated into different categories:

1. Ensuring the [**required policies**](#required-policies) for Update Compliance are correctly configured.
2. Devices in every network topography needs to send data to the [**required endpoints**](#required-endpoints) for Update Compliance, for example both devices in main and satellite offices, which may have different network configurations.
3. Ensure [**Required Windows services**](#required-services) are running or are scheduled to run. It is recommended all Microsoft and Windows services are set to their out-of-box defaults to ensure proper functionality.

## Required policies

> [!NOTE]
> Windows 10 MDM and Group Policies are backed by registry keys. It is not recommended you set these registry keys directly for configuration as it can lead to unexpected behavior, so the exact registry key locations are not provided, though they are referenced for troubleshooting configuration issues with the [Update Compliance Configuration Script](update-compliance-configuration-script.md).

Update Compliance has a number of policies that must be appropriately configured in order for devices to be processed by Microsoft and visible in Update Compliance. They are enumerated below, separated by whether the policies will be configured via [Mobile Device Management](https://docs.microsoft.com/windows/client-management/mdm/) (MDM) or Group Policy. For both tables:

- **Policy** corresponds to the location and name of the policy.
- **Value** Indicates what value the policy must be set to. Update Compliance requires *at least* Basic (or Required) telemetry, but can function off Enhanced or Full (or Optional).
- **Function** details why the policy is required and what function it serves for Update Compliance. It will also detail a minimum version the policy is required, if any.

### Mobile Device Management policies

Each MDM Policy links to its documentation in the CSP hierarchy, providing its exact location in the hierarchy and more details.

| Policy | Value | Function |
|---------------------------|-|------------------------------------------------------------|
|**Provider/*ProviderID*/**[**CommercialID**](https://docs.microsoft.com/windows/client-management/mdm/dmclient-csp#provider-providerid-commercialid) |[Your CommercialID](update-compliance-get-started.md#get-your-commercialid) |Identifies the device as belonging to your organization. |
|**System/**[**AllowTelemetry**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-system#system-allowtelemetry) |1- Basic |Configures the maximum allowed telemetry to be sent to Microsoft. Individual users can still set this lower than what the policy defines, see the below policy for more information. |
|**System/**[**ConfigureTelemetryOptInSettingsUx**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-system#system-configuretelemetryoptinsettingsux) | Disable Telemetry opt-in Settings | (*Windows 10 1803+*) Determines whether end-users of the device can adjust telemetry to levels lower than the level defined by AllowTelemetry. It is recommended you disable this policy order the effective telemetry level on devices may not be sufficient. |
|**System/**[**AllowDeviceNameInDiagnosticData**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-system#system-allowdevicenameindiagnosticdata) | 1 - Allowed | Allows device name to be sent for Windows Diagnostic Data. If this policy is Not Configured or set to 0 (Disabled), Device Name will not be sent and will not be visible in Update Compliance, showing `#` instead. |

### Group Policies

All Group Policies that need to be configured for Update Compliance are under **Computer Configuration>Administrative Templates>Windows Components\Data Collection and Preview Builds**. All of these policies must be in the *Enabled* state and set to the defined *Value* below.  

| Policy | Value | Function |
|---------------------------|-|-----------------------------------------------------------|
|**Configure the Commercial ID** |[Your CommercialID](update-compliance-get-started.md#get-your-commercialid) | Identifies the device as belonging to your organization. |
|**Allow Telemetry** | 1 - Basic |Configures the maximum allowed telemetry to be sent to Microsoft. Individual users can still set this lower than what the policy defines, see the below policy for more information. |
|**Configure telemetry opt-in setting user interface** | Disable telemetry opt-in Settings |(*Windows 10 1803+*) Determines whether end-users of the device can adjust telemetry to levels lower than the level defined by AllowTelemetry. It is recommended you disable this policy order the effective telemetry level on devices may not be sufficient. |
|**Allow device name to be sent in Windows diagnostic data** | Enabled | Allows device name to be sent for Windows Diagnostic Data. If this policy is Not Configured or Disabled, Device Name will not be sent and will not be visible in Update Compliance, showing `#` instead. |

## Required endpoints

To enable data sharing between devices, your network, and Microsoft's Diagnostic Data Service, configure your proxy to allow devices to contact the below endpoints.

| **Endpoint**  | **Function**  |
|---------------------------------------------------------|-----------|
| `https://v10c.events.data.microsoft.com` | Connected User Experience and Diagnostic component endpoint for Windows 10, version 1803 and later. Census.exe must run on a regular cadence and contact this endpoint in order to receive the majority of [WaaSUpdateStatus](update-compliance-schema-waasupdatestatus.md) information for Update Compliance. |
| `https://v10.vortex-win.data.microsoft.com` | Connected User Experience and Diagnostic component endpoint for Windows 10, version 1709 or earlier. |
| `https://settings-win.data.microsoft.com` | Required for Windows Update functionality. |
| `http://adl.windows.com` | Required for Windows Update functionality. |
| `https://watson.telemetry.microsoft.com` | Windows Error Reporting (WER), used to provide more advanced error reporting in the event of certain Feature Update deployment failures. |
| `https://oca.telemetry.microsoft.com`  | Online Crash Analysis, used to provide device-specific recommendations and detailed errors in the event of certain crashes. |
| `https://login.live.com` | This endpoint facilitates MSA access and is required to create the primary identifier we use for devices. Without this service, devices will not be visible in the solution. This also requires Microsoft Account Sign-in Assistant service to be running (wlidsvc). |

## Required services

Many Windows and Microsoft services are required to ensure that not only the device can function, but Update Compliance can see device data. It is recommended that you allow all default services from the out-of-box experience to remain running. The [Update Compliance Configuration Script](update-compliance-configuration-script.md) checks whether the majority of these services are running or are allowed to run automatically.
