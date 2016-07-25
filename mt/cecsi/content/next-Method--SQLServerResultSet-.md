---
title: "next-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.next
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 60248447-6908-4036-a779-a501453cd553
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
# next-Methode (ISQLServerResultSet)
    
## next\-Methode \(ISQLServerResultSet\)  
 Versetzt den Cursor von seiner aktuellen Position aus um eine Zeile nach unten.  
  
## Syntax  
  
```  
  
public boolean next()  
```  
  
## Rückgabewert  
 **true**, wenn die neue Parallelitätszeile gültig ist. **false**, wenn keine Zeilen mehr zur Bearbeitung vorhanden sind.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese next\-Methode wird von der next\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Ein Resultsetcursor wird anfänglich vor dieser Zeile positioniert. Beim ersten Aufruf der next\-Methode wird die erste Zeile zur aktuellen Zeile, beim zweiten Aufruf wird die zweite Zeile zur aktuellen Zeile usw.  
  
 Wenn für die aktuelle Zeile ein Eingabedatenstrom geöffnet ist, wird dieser durch einen Aufruf der next\-Methode implizit geschlossen. Beim Lesen einer neuen Zeile wird eine Warnkette für das [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt gelöscht.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  