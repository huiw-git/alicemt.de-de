---
title: "getWarnings-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.getWarnings
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 15af39bf-6285-44cc-a021-7341e7a055c4
caps.latest.revision: 8
caps.handback.revision: 8
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
# getWarnings-Methode (ISQLServerConnection)
    
## getWarnings\-Methode \(ISQLServerConnection\)  
 Ruft die erste Warnung ab, die von Aufrufen für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt gemeldet wurde.  
  
## Syntax  
  
```  
  
public java.sql.SQLWarning getWarnings()  
```  
  
## Rückgabewert  
 Ein SQLWarning\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getWarnings\-Methode wird von der getWarnings\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Darauffolgende Warnungen werden an das erste SQLWarning\-Element angehängt und mit der getNextWarning\-Methode aufgerufen. Beim Aufruf für eine geschlossene Verbindung wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  