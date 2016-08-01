---
title: "getBigDecimal-Methode (int, int)"
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
  - SQLServerCallableStatement.getBigDecimal (int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d9351b35-7046-4852-a612-72d4c46b2bbb
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
# getBigDecimal-Methode (int, int)
    
## getBigDecimal\-Methode \(int, int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes und der Dezimalstellen als java.math.BigDecimal\-Objekt ab.  
  
> [!NOTE]  
>  Diese Methode gilt in der JDBC\-Spezifikation als veraltet. Verwenden Sie stattdessen die [getBigDecimal \(int\)](../content/getBigDecimal-Method--int-.md)\-Methode.  
  
## Syntax  
  
```  
  
public java.math.BigDecimal getBigDecimal(int index,  
                                          int scale)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
 *scale*  
  
 Ein Element vom Typ **int** , das die Anzahl von Stellen rechts des Dezimalzeichens anzeigt.  
  
## Rückgabewert  
 Ein BigDecimal\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBigDecimal\-Methode wird von der getBigDecimal\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getBigDecimal-Methode &#40;SQLServerCallableStatement&#41;](../content/getBigDecimal-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  