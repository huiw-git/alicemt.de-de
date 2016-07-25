---
title: "executeBatch-Methode (SQLServerPreparedStatement)"
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
  - SQLServerPreparedStatement.executeBatch
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8418167e-cbd2-464d-b118-73cdd76080ed
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
# executeBatch-Methode (SQLServerPreparedStatement)
  Übermittelt einen Befehlsbatch zur Ausführung an die Datenbank. Werden alle Befehle erfolgreich ausgeführt, wird ein Array mit Updatezählungen zurückgegeben.  
  
## Syntax  
  
```  
  
public int[] executeBatch()  
```  
  
## Rückgabewert  
 Ein Array aus int\-Elementen, das die Updatezählungen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
 java.sql.BatchUpdateException  
  
## Hinweise  
 Diese executeBatch\-Methode wird von der executeBatch\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 ist kompatibel mit der JDBC 4.0\-Empfehlung, dass bei einem Aufruf der CallableStatement.executeBatch\-Methode \(geerbt von PreparedStatement\) eine BatchUpdateException ausgelöst wird, wenn die gespeicherte Prozedur OUT\- oder INOUT\-Parameter akzeptiert oder andere Daten als eine Updatezählung zurückgibt.  
  
 Diese Methode überschreibt [SQLServerStatement.executeBatch](../content/executeBatch-Method--SQLServerStatement-.md).  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  