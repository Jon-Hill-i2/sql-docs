---
description: "MSSQLSERVER_33028"
title: "MSSQLSERVER_33028 | Microsoft Docs"
ms.custom: ""
ms.date: "04/04/2017"
ms.service: sql
ms.reviewer: ""
ms.subservice: supportability
ms.topic: "reference"
helpviewer_keywords: 
  - "33028 (Database Engine error)"
ms.assetid: c5cec0e4-0bcd-4907-826f-e7d835cfcb37
author: MashaMSFT
ms.author: mathoma
---
# MSSQLSERVER_33028
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## Details  
  
| Attribute | Value |  
| :-------- | :---- |  
|Product Name|SQL Server|  
|Event ID|33028|  
|Event Source|MSSQLSERVER|  
|Component|SQLEngine|  
|Symbolic Name|SEC_CRYPTOPROV_CANTOPENSESSION|  
|Message Text|Cannot open session for %S_MSG '%.*ls'. Provider error code: %d.|  
  
## Explanation  
[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] was unable to open the cryptographic provider listed in the error message. The cryptographic provider supplied the error code listed. You may need to contact your cryptographic provider for more information about the error.  
  
|Error code|Description|  
|--------------|---------------|  
|0|Success. No error.|  
|1|Failure. An unspecified or unexpected error occurred. Additional information is not available.|  
|2|Insufficient Buffer. Space could not be allocated for the cryptographic provider.|  
|3|Not Supported. The cryptographic provider is not supported by this release. Select another cryptographic provider.|  
|4|Not Found. The specified cryptographic provider is not present or you do not have authorization to access the files.|  
|5|Authorization Failure. Can result from providing an incorrect password or username when creating the credential. Can result if the credential does not exist.|  
|6|Invalid Argument. An invalid argument was passed to the cryptographic provider.|  
  
## User Action  
Resolve the error, or contact the cryptographic provider for more information.  
  
