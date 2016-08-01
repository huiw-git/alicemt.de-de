---
title: "getAutoCommit-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.getAutoCommit
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: af1f67f4-f568-4e58-abcc-5c809a89b547
caps.latest.revision: 10
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
# getAutoCommit-Methode (ISQLServerConnection)
    
## getAutoCommit\-Methode \(ISQLServerConnection\)  
 Ruft für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt den aktuellen Modus für automatische Commits ab.  
  
## Syntax  
  
```  
  
public boolean getAutoCommit()  
```  
  
## Rückgabewert  
 **true**, sofern automatische Commits aktiviert sind. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getAutoCommit\-Methode wird von der getAutoCommit\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  