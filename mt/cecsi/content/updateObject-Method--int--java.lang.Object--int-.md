---
title: "updateObject-Methode (int, java.lang.Object, int)"
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
  - SQLServerResultSet.updateObject (int, java.lang.Object, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9d33571b-4887-49d3-96df-8abda7b5a904
caps.latest.revision: 15
caps.handback.revision: 15
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
# updateObject-Methode (int, java.lang.Object, int)
    
## updateObject\-Methode \(int, java.lang.Object, int\)  
 Aktualisiert die angegebene Spalte mit einem Wert vom Typ **Object** unter Verwendung des angegebenen Spaltenindexes und der Dezimalstellen.  
  
## Syntax  
  
```  
  
public void updateObject(int index,  
                         java.lang.Object x,  
                         int scale)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *obj*  
  
 Ein **Object** \-Wert.  
  
 *scale*  
  
 Gilt für java.sql.Types.DECIMAL\- oder java.sql.Types.NUMERIC\-Typen. Dieser Wert gibt die Anzahl der Dezimalstellen an. Bei allen anderen Typen wird dieser Wert ignoriert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Siehe auch  
 [updateObject-Methode &#40;SQLServerResultSet&#41;](../content/updateObject-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  