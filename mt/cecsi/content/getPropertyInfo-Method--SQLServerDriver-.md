---
title: "getPropertyInfo-Methode (SQLServerDriver)"
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
  - SQLServerDriver.getPropertyInfo
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b5eaad8a-31ef-44ac-af11-d5caa13ac3e2
caps.latest.revision: 7
caps.handback.revision: 7
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
# getPropertyInfo-Methode (SQLServerDriver)
    
## getPropertyInfo\-Methode \(SQLServerDriver\)  
 Dient zum Ermitteln der erforderlichen Eigenschaften zum Herstellen einer Datenbankverbindung.  
  
## Syntax  
  
```  
  
public java.sql.DriverPropertyInfo[] getPropertyInfo(java.lang.String Url,  
                                                     java.util.Properties Info)  
```  
  
#### Parameter  
 *Url*  
  
 Ein **String** \-Wert mit der URL, die zum Herstellen einer Verbindung mit der Datenbank verwendet wird.  
  
 *Info*  
  
 Eine Liste mit Eigenschaftswertpaaren \(bei der ersten Verwendung NULL\).  
  
## Rückgabewert  
 Ein Array mit DriverPropertyInfo\-Objekten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getPropertyInfo\-Methode wird von der getPropertyInfo\-Methode in der java.sql.Driver\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDriver-Methoden](../content/SQLServerDriver-Methods.md)   
 [SQLServerDriver-Elemente](../content/SQLServerDriver-Members.md)   
 [SQLServerDriver-Klasse](../content/SQLServerDriver-Class.md)  
  
  