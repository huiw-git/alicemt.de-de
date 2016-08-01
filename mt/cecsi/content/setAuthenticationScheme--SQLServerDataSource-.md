---
title: "setAuthenticationScheme (SQLServerDataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b942f78e-7ce1-44ef-923d-a7c3d7c76b83
caps.latest.revision: 4
caps.handback.revision: 4
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - sv-se
  - zh-cn
  - zh-tw
---
# setAuthenticationScheme (SQLServerDataSource)
  Gibt die Art der integrierten Sicherheit an, die für die Anwendung verwendet werden soll.  
  
## Syntax  
  
```vb  
public void setAuthenticationScheme(String authenticationScheme);  
```  
  
#### Parameter  
 *authenticationScheme*  
  
 Werte sind **"JavaKerberos"** und die standardmäßige **"NativeAuthentication"**. Weitere Informationen finden Sie unter [Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung](../content/Using-Kerberos-Integrated-Authentication-to-Connect-to-SQL-Server.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  