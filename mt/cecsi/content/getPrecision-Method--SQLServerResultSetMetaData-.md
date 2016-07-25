---
title: "getPrecision-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getPrecision
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: de46c96e-6ad6-4946-883e-807123658500
caps.latest.revision: 7
caps.handback.revision: 7
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
# getPrecision-Methode (SQLServerResultSetMetaData)
    
## getPrecision\-Methode \(SQLServerResultSetMetaData\)  
 Ruft die Anzahl von Dezimalstellen der angegebenen Spalte ab.  
  
## Syntax  
  
```  
  
public int getPrecision(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Genauigkeit der Spalte.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getPrecision\-Methode wird von der getPrecision\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  