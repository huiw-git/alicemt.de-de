---
title: "updateArray-Methode (int, java.sql.Array)"
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
  - SQLServerResultSet.updateArray (int, java.sql.Array)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 464f7e3f-3e8a-4b2d-aebd-1c040583d52c
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
# updateArray-Methode (int, java.sql.Array)
    
## updateArray\-Methode \(int, java.sql.Array\)  
 Aktualisiert die angegebene Spalte mit einem Array\-Objekt unter Berücksichtigung des Spaltenindexes.  
  
## Syntax  
  
```  
  
public void updateArray(int columnIndex,  
                        java.sql.Array x)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *x*  
  
 Ein Array\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateArray\-Methode wird von der updateArray\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateArray-Methode &#40;ISQLServerResultSet&#41;](../content/updateArray-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  