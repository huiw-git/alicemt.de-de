---
title: "getShort-Methode (int) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getShort (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0b543c92-feb8-46a4-8477-9b5f94f1cdc7
caps.latest.revision: 9
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
# getShort-Methode (int) (ISQLServerResultSet)
    
## getShort\-Methode \(int\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **short** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public short getShort(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **short** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getShort\-Methode wird von der getShort\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Die Methode wird nur unter [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen unterstützt, die einen Ganzzahlwert wie "smallint", "tinyint" und "bit" sicher zurückgeben. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getShort-Methode &#40;ISQLServerResultSet&#41;](../content/getShort-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  