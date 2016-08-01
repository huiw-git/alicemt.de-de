---
title: "finalize-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.finalize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 49bc879d-822b-42da-bc20-2394865f1f0f
caps.latest.revision: 9
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
# finalize-Methode (ISQLServerResultSet)
    
## finalize\-Methode \(ISQLServerResultSet\)  
 Schließt dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt explizit.  
  
## Syntax  
  
```  
  
public void finalize()  
```  
  
## Hinweise  
 Schließt das Resultset, wenn dies nicht durch die Anwendung geschieht. Diese Methode entspricht der JDBC\-Spezifikation. Da die Java Virtual Machine \(JVM\) keine Garantie dafür bietet, wann ein Finalizer ausgeführt werden kann, können Anwendungen, von denen ihre Resultsets nicht explizit geschlossen werden, einen Deadlock für eine andere Anweisung auslösen, von der die gleiche Verbindung verwendet wird und die für eine gemeinsame Serverressource \(z. B. Zeilensperren\) blockiert wird.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  