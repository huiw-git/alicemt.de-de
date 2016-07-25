---
title: "getFloat-Methode (int) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getFloat (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 30863ef5-7a7c-440e-8fbb-426a99266ee1
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
# getFloat-Methode (int) (ISQLServerResultSet)
    
## getFloat\-Methode \(int\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **float** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public float getFloat(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **float** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getFloat\-Methode wird von der getFloat\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden alle zahlenbasierten Typen mit der Java\-Genauigkeit vom Typ **float** zurückgegeben.  
  
## Siehe auch  
 [getFloat-Methode &#40;ISQLServerResultSet&#41;](../content/getFloat-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  