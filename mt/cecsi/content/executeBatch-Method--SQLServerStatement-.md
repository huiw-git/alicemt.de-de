---
title: "executeBatch-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.executeBatch
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fb034f63-2532-4da8-a1b0-bc125734585a
caps.latest.revision: 11
caps.handback.revision: 11
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
# executeBatch-Methode (ISQLServerStatement)
    
## executeBatch\-Methode \(ISQLServerStatement\)  
 Übermittelt einen Befehlsbatch zur Ausführung an die Datenbank. Werden alle Befehle erfolgreich ausgeführt, wird ein Array mit Updatezählungen zurückgegeben.  
  
## Syntax  
  
```  
  
public int[] executeBatch()  
```  
  
## Rückgabewert  
 Ein Array aus **int**\-Elementen, die Updatezählungen enthalten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
 java.sql.BatchUpdateException  
  
## Hinweise  
 Diese executeBatch\-Methode wird von der executeBatch\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Nach dem Übertragen von Befehlen an die Datenbank werden von der Methode alle Befehle im Stapel gelöscht.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  