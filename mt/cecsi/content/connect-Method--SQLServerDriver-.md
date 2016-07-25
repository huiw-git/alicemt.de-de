---
title: "connect-Methode (SQLServerDriver)"
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
  - SQLServerDriver.connect
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 43813a4c-1cc7-4659-ba27-f1786f1371eb
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
# connect-Methode (SQLServerDriver)
    
## connect\-Methode \(SQLServerDriver\)  
 Stellt eine Verbindung mit der Datenbank her.  
  
## Syntax  
  
```  
  
public java.sql.Connection connect(java.lang.String Url,  
                                   java.util.Properties suppliedProperties)  
```  
  
#### Parameter  
 *Url*  
  
 Ein **String** \-Wert mit der URL, die zum Herstellen einer Verbindung mit der Datenbank verwendet wird.  
  
 *suppliedProperties*  
  
 Ein Satz von Stringwertpaaren, die als Verbindungsargumente verwendet werden.  
  
## Rückgabewert  
 Ein Connection\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese connect\-Methode wird von der connect\-Methode in der java.sql.Driver\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDriver-Methoden](../content/SQLServerDriver-Methods.md)   
 [SQLServerDriver-Elemente](../content/SQLServerDriver-Members.md)   
 [SQLServerDriver-Klasse](../content/SQLServerDriver-Class.md)  
  
  