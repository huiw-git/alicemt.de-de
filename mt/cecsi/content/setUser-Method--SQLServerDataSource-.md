---
title: "setUser-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setUser
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d2ea7906-2d10-438d-aa51-f576eea923c7
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
# setUser-Methode (SQLServerDataSource)
    
## setUser\-Methode \(SQLServerDataSource\)  
 Legt den Benutzernamen fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## Syntax  
  
```  
  
public void setUser(java.lang.String user)  
```  
  
#### Parameter  
 *user*  
  
 Ein **String** mit dem Benutzernamen.  
  
## Hinweise  
 Von der setUser\-Methode wird das Kennwort festgelegt, das für die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird. Ist der Wert für den Benutzernamen nicht festgelegt, wird von der [getUser](../content/getUser-Method--SQLServerDataSource-.md)\-Methode der Standardwert \(NULL\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  