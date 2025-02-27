---
title: Gather information by using TSS for Active Directory replication issues
description: Introduces how to gather information by using the TroubleShootingScript (TSS) toolset for Active Directory replication issues.
ms.date: 07/13/2023
manager: dcscontentpm
audience: itpro
ms.topic: troubleshooting
ms.prod: windows-client
localization_priority: medium
ms.reviewer: kaushika, warrenw, v-lianna
ms.custom: sap:windows-tss-ds, csstroubleshoot
ms.technology: windows-client-troubleshooter
---
# Gather information by using TSS for Active Directory replication issues

This article introduces how to gather information by using the TroubleShootingScript (TSS) toolset for Active Directory replication issues.

Before contacting Microsoft support, you can gather information about your issue.

## Prerequisites

Refer to [Introduction to TroubleShootingScript toolset (TSS)](introduction-to-troubleshootingscript-toolset-tss.md#prerequisites) for prerequisites for the toolset to run properly.

## Gather key information before contacting Microsoft support

1. Download [TSS](https://aka.ms/getTSS) and extract it in the *C:\\tss* folder.
2. Open the *C:\\tss* folder from an elevated PowerShell command prompt.  
    > [!NOTE]
    > Don't use the Windows PowerShell Integrated Scripting Environment (ISE).
3. Run the following cmdlets:

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

    ```powershell
    .\TSS.ps1 -Scenario ADS_General -noProcmon -noPSR -noVideo
    ```

4. Enter *A* for "Yes to All" for the execution policy change.

> [!NOTE]
>
> - The traces are stored in a compressed file in the *C:\\MS_DATA* folder. After a support case is created, this file can be uploaded to the secure workspace for analysis.
> - If you've downloaded this tool previously, we recommend downloading the latest version. It doesn't automatically update when running `-Scenario ADS_General -noProcmon -noPSR -noVideo`.
