---
title: "getMaxRows-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.getMaxRows
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6aece4e5-027d-434e-a8cf-a67c0484f189
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
# getMaxRows-Methode (ISQLServerStatement)
    
## getMaxRows\-Methode \(ISQLServerStatement\)  
 Ruft die maximale Anzahl von Zeilen ab, die ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, das von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt wird.  
  
## Syntax  
  
```  
  
public final int getMaxRows()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der maximalen Zeilenanzahl \("0", wenn kein Limit vorhanden ist\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMaxRows\-Methode wird von der getMaxRows\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Die getMaxRows\-Methode gibt für dynamische, scrollfähige Cursor immer 0 zurück.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  