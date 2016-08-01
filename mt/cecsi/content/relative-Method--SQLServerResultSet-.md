---
title: "relative-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.relative
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2bcdbb69-95fd-4ae8-8488-1a75a91fe2e0
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
# relative-Methode (ISQLServerResultSet)
    
## relative\-Methode \(ISQLServerResultSet\)  
 Versetzt den Cursor relativ zur aktuellen Zeile um eine bestimmte \(positive oder negative\) Anzahl von Zeilen.  
  
## Syntax  
  
```  
  
public boolean relative(int nRows)  
```  
  
#### Parameter  
 *nRows*  
  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der zu verschiebenden Zeilen.  
  
## Rückgabewert  
 **true**, wenn sich der Cursor in einer Zeile befindet. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese relative\-Methode wird von der relative\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Wenn versucht wird, den Cursor über die erste oder letzte Zeile im Resultset hinaus zu verschieben, wird er vor oder hinter der ersten bzw. letzten Reihe positioniert. Der Aufruf von `relative(0)` ist gültig, hat jedoch keine Auswirkungen auf die Position des Cursors.  
  
 Der Aufruf der Methode `relative(1)` ist mit dem Aufruf der [next](../content/next-Method--SQLServerResultSet-.md)\-Methode identisch. Der Aufruf der Methode `relative(-1)` ist mit dem Aufruf der [previous](../content/previous-Method--SQLServerResultSet-.md)\-Methode identisch.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  