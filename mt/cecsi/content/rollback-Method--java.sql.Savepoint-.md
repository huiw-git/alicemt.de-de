---
title: "rollback-Methode (java.sql.Savepoint)"
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
  - SQLServerConnection.rollback (java.sql.Savepoint)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d5dbd9ef-194f-4130-bfcc-7901a4fa8ded
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
# rollback-Methode (java.sql.Savepoint)
    
## rollback\-Methode \(java.sql.Savepoint\)  
 Macht alle nach dem Festlegen des vorhandenen [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekts festgelegten Änderungen rückgängig.  
  
## Syntax  
  
```  
  
public void rollback(java.sql.Savepoint s)  
```  
  
#### Parameter  
 *s*  
  
 Das SavePoint\-Objekt, bis zu dem das Rollback durchgeführt werden soll.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese rollBack\-Methode wird von der rollBack\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Die Methode sollte nur bei deaktiviertem Modus für automatische Commits verwendet werden.  
  
## Siehe auch  
 [rollback-Methode &#40;ISQLServerConnection&#41;](../content/rollback-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  