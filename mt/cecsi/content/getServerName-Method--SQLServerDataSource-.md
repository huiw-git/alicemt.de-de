---
title: "getServerName-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getServerName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3004ed22-5d69-4dd0-8761-d39f0b7dde13
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
# getServerName-Methode (SQLServerDataSource)
    
## getServerName\-Methode \(SQLServerDataSource\)  
 Gibt den Namen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz zurück.  
  
## Syntax  
  
```  
  
public java.lang.String getServerName()  
```  
  
## Rückgabewert  
 Ein **String** , der den Servernamen oder NULL enthält, sofern kein Wert festgelegt ist.  
  
## Hinweise  
 Der Servername ist der Hostname des Zielcomputers, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird. Ist die getServerName\-Eigenschaft nicht festgelegt, wird von getServerName der Standardwert \(NULL\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  