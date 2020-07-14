---
title: Update Compliance Data Schema
ms.reviewer: 
manager: laurawi
description: an overview of Update Compliance data schema
ms.prod: w10
ms.mktglfcycl: deploy
ms.pagetype: deploy
audience: itpro
itproauthor: jaimeo
author: jaimeo
ms.author: jaimeo
ms.collection: M365-analytics
ms.topic: article
---

# Update Compliance Schema

When the visualizations provided in the default experience don't fulfill your reporting needs, or if you need to troubleshoot issues with devices, it's valuable to understand the schema for Update Compliance and have a high-level understanding of the capabilities of [Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/query-language) to power additional dashboards, integration with external data analysis tools, automated alerting, and more.

The table below summarizes the different tables that are part of the Update Compliance solution. To learn how to navigate Azure Monitor Logs to find this data, see [Get started with log queries in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries).

|Table |Category |Description |
|--|--|--|
|[**WaaSUpdateStatus**](update-compliance-schema-waasupdatestatus.md) |Device record |This table houses device-centric data and acts as the device record for Update Compliance. Each record provided in daily snapshots map to a single device in a single tenant. This table has data such as the current device's installed version of Windows, whether it is on the latest available updates, and whether the device needs attention. |
|[**WaaSInsiderStatus**](update-compliance-schema-waasinsiderstatus.md) |Device record |This table houses device-centric data specifically for devices enrolled to the Windows Insider Program. Devices enrolled to the Windows Insider Program do not currently have any WaaSDeploymentStatus records, so do not have Update Session data to report on update deployment progress. |
|[**WaaSDeploymentStatus**](update-compliance-schema-waasdeploymentstatus.md) |Update Session record |This table tracks a specific update on a specific device. Multiple WaaSDeploymentStatus records can exist simultaneously for a given device, as each record is specific to a given update and its type. For example, a device can have both a WaaSDeploymentStatus tracking a Windows Feature Update, as well as one tracking a Windows Quality Update, at the same time. |
|[**WUDOStatus**](update-compliance-schema-wudostatus.md) |Delivery Optimization record |This table provides information, for a single device, on their bandwidth utilization across content types in the event they use [Delivery Optimization](https://support.microsoft.com/help/4468254/windows-update-delivery-optimization-faq). |
|[**WUDOAggregatedStatus**](update-compliance-schema-wudoaggregatedstatus.md) |Delivery Optimization record |This table aggregates all individual WUDOStatus records across the tenant and summarizes bandwidth savings across all devices enrolled to Delivery Optimization. |
