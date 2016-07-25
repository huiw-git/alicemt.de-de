---
title: "findColumn-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.findColumn
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7c29994a-0b53-420b-8a9b-82a9eef08587
caps.latest.revision: 12
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
# findColumn-Methode (ISQLServerResultSet)
    
## findColumn\-Methode \(ISQLServerResultSet\)  
 Ruft für den angegebenen Spaltennamen den Index der ersten übereinstimmenden Spalte in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.  
  
## Syntax  
  
```  
  
public int findColumn(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese findColumn\-Methode wird von der findColumn\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Sind mehrere Spalten mit dem gleichen Namen vorhanden, wird von der findColumn\-Methode die erste die Groß\-\/Kleinschreibung berücksichtigende Übereinstimmung zurückgegeben. Ist keine Groß\-\/Kleinschreibung berücksichtigende Übereinstimmung vorhanden, wird von der Methode die erste die Groß\-\/Kleinschreibung nicht berücksichtigende Übereinstimmung zurückgegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  