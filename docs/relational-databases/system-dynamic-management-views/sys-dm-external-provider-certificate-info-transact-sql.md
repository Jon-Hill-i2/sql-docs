---
title: "sys.dm_external_provider_certificate_info (Transact-SQL)"
description: sys.dm_external_provider_certificate_info (Transact-SQL)
author: GithubMirek
ms.author: mireks
ms.date: "02/15/2023"
ms.service: sql
ms.subservice: system-objects
ms.topic: "reference"
---
# sys.dm_external_provider_certificate_info (Transact-SQL)
[!INCLUDE [sqlserver2022](../../includes/applies-to-version/sqlserver2022.md)]

> [!NOTE]
> This view is introduced in SQL Server 2022 CU1.

Returns information about the Azure cloud certificates used in SQL Server to set up and maintain an Azure AD administrator required to support Azure AD authentication. For more information, see [Set up Azure Active Directory authentication for SQL Server](/sql/relational-databases/security/authentication-access/azure-ad-authentication-sql-server-setup-tutorial).
  
|Column name|Data type|Description|  
|-----------------|---------------|-----------------|  
|**Subject**|**nvarchar(4000)**|The subject name of the certificate.|  
|**thumbprint**|**nvarchar(4000)**|Certificate thumbprint.|  
|**expire_date**|**datetime2**|Certificate expiration date and time.|  
|**is_readable**|**bit**|Indicates whether the certificate is readable for both public and private key. </br> </br> Values are: </br> 1 - Yes </br> 0 - No|  
|**is_missing**|**bit**|Indicates whether the certificate is present in the certificate store. </br> </br> Values are: </br> 1 - Yes </br> 0 - No|  
  
## Permissions

Principals must have the **VIEW SERVER SECURITY STATE** permission.
  
The visibility of the metadata in catalog views is limited to securables that a user either owns or on which the user has been granted some permission. For more information, see [Metadata Visibility Configuration](/sql/relational-databases/security/metadata-visibility-configuration).
  
## See also

- [Set up Azure Active Directory authentication for SQL Server](/sql/relational-databases/security/authentication-access/azure-ad-authentication-sql-server-setup-tutorial)
- [Azure Active Directory authentication for SQL Server](/sql/relational-databases/security/authentication-access/azure-ad-authentication-sql-server-overview)
- [Linked server for SQL Server with Azure Active Directory authentication](/sql/relational-databases/security/authentication-access/azure-ad-authentication-sql-server-linked-server)
- [Tutorial: Using automation to set up the Azure Active Directory admin for SQL Server](/sql/relational-databases/security/azure-ad-authentication-sql-server-automation-setup-tutorial.md)
