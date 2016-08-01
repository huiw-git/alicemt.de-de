---
title: "getUser-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.getUser
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3513dd7f-6ae5-4010-bde0-454ac4365bce
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
# getUser-Methode (SQLServerDataSource)
    
## getUser\-Methode \(SQLServerDataSource\)  
 Gibt den Benutzernamen zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## Syntax  
  
```  
  
public java.lang.String getUser()  
```  
  
## Rückgabewert  
 Ein **String** mit dem Benutzernamen.  
  
## Hinweise  
 Von der [setUser](../content/setUser-Method--SQLServerDataSource-.md)\-Methode wird der Benutzername festgelegt, der beim Herstellen einer Verbindung zur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz verwendet wird. Ist der Wert für den Benutzernamen nicht festgelegt, wird von der getUser\-Methode der Standardwert \(NULL\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  