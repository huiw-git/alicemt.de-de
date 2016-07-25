---
title: "getBigDecimal-Methode (int, int) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getBigDecimal (int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c99d0772-b26c-492c-a643-2813b5429993
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
# getBigDecimal-Methode (int, int) (ISQLServerResultSet)
    
## getBigDecimal\-Methode \(int, int\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts unter Verwendung der angegebenen Dezimalstellen ab.  
  
> [!NOTE]  
>  Diese Methode gilt in der JDBC\-Spezifikation als veraltet. Verwenden Sie stattdessen die [getBigDecimal \(int\)](../content/getBigDecimal-Method--int---SQLServerResultSet-.md)\-Methode.  
  
## Syntax  
  
```  
  
public java.math.BigDecimal getBigDecimal(int columnIndex,  
                                          int scale)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *scale*  
  
 Ein Element vom Typ **int** , das die Anzahl von Stellen rechts des Dezimalzeichens anzeigt.  
  
## Rückgabewert  
 Ein BigDecimal\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBigDecimal\-Methode wird von der getBigDecimal\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getBigDecimal-Methode &#40;ISQLServerResultSet&#41;](../content/getBigDecimal-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  