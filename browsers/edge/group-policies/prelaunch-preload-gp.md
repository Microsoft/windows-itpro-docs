---
title: Microsoft Edge - Prelaunch and tab preload configuration options
description: Microsoft Edge pre-launches as a background process during Windows startup when the system is idle waiting to be launched by the user.  Pre-launching helps the performance of Microsoft Edge and minimizes the amount of time required to start up Microsoft Edge.
ms.author: pashort
author: shortpatti
ms.date: 07/25/2018
---

# Prelaunch Microsoft Edge and preload tabs in the background  
>*Supported versions: Microsoft Edge on Windows 10, next major update to Windows*


Microsoft Edge pre-launches as a background process during Windows startup when the system is idle waiting to be launched by the user.  Pre-launching helps the performance of Microsoft Edge and minimizes the amount of time required to start up Microsoft Edge. You can also configure Microsoft Edge to prevent Microsoft Edge from pre-launching.  

Additionally, Microsoft Edge preloads the Start and New tab pages during Windows sign in, which minimizes the amount of time required to start Microsoft Edge and load a new tab.  You can also configure Microsoft Edge to prevent preloading of tabs. 


## Relevant group policies

- [Allow Microsoft Edge to pre-launch at Windows startup, when the system is idle, and each time Microsoft Edge is closed](#allow-microsoft-edge-to-pre-launch-at-windows-startup-when-the-system-is-idle-and-each-time-microsoft-edge-is-closed)
- [Allow Microsoft Edge to load the Start and New Tab page at Windows startup and each time Microsoft Edge is closed](#allow-microsoft-edge-to-start-and-load-the-start-and-new-tab-page-at-windows-startup-and-each-time-microsoft-edge-is-closed)


## Configuration options

![Only preload the Start and New tab pages during Windows startup](../images/preload-tabs-only-sm.png)

![Prelauch Microsoft Edge and preload Start and New tab pages](../images/prelaunch-edge-and-preload-tabs-sm.png)

![Only prelaunch Microsoft Edge during Windows startup](../images/prelaunch-edge-only-sm.png)



## Allow Microsoft Edge to pre-launch at Windows startup, when the system is idle, and each time Microsoft Edge is closed
[!INCLUDE [allow-prelaunch-include](../includes/allow-prelaunch-include.md)]

## Allow Microsoft Edge to load the Start and New Tab page at Windows startup and each time Microsoft Edge is closed
[!INCLUDE [allow-tab-preloading-include](../includes/allow-tab-preloading-include.md)]