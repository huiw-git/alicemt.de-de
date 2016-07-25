---
title: "setServerName-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.setServerName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 70920828-eda0-4064-be9f-c1e460db8f00
caps.latest.revision: 9
caps.handback.revision: 9
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
# setServerName-Methode (SQLServerDataSource)
    
## setServerName\-Methode \(SQLServerDataSource\)  
 Legt den Namen des Computers fest, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.  
  
## Syntax  
  
```  
  
public void setServerName(java.lang.String serverName)  
```  
  
#### Parameter  
 *serverName*  
  
 Ein **String** mit dem Namen des Servers.  
  
## Hinweise  
 Der Servername ist der Hostname des Zielcomputers, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird. Ist die serverName\-Eigenschaft nicht festgelegt, wird von [getServerName](../content/getServerName-Method--SQLServerDataSource-.md) der Standardwert \(NULL\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  