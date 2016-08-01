---
title: "getColumnLabel-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getColumnLabel
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: cf67692c-24aa-49e6-8e88-a47d4e8c021c
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
# getColumnLabel-Methode (SQLServerResultSetMetaData)
    
## getColumnLabel\-Methode \(SQLServerResultSetMetaData\)  
 Ruft für die angegebene Spalte den vorgeschlagenen Titel für Ausdrucke und Anzeigen ab.  
  
## Syntax  
  
```  
  
public java.lang.String getColumnLabel(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein **String** mit dem Spaltentitel.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getColumnLabel\-Methode wird von der getColumnLabel\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
 Die Methode gibt den Aliasnamen der Spalte zurück. Ist dieser nicht verfügbar, wird von der Methode der Spaltenname zurückgegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  