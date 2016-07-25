---
title: "getNClob-Methode (int) (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 103082e3-de98-4dff-8dc7-eaa5c64b1597
caps.latest.revision: 16
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
# getNClob-Methode (int) (SQLServerResultSet)
  Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als NClob\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.NClob getNClob(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
## Rückgabewert  
 Ein NClob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getNClob\-Methode wird von der getNClob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Spalten vom Typ **nvarchar\(max\)**, **ntext** und **xml** unterstützt. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getNClob-Methode &#40;SQLServerResultSet&#41;](../content/getNClob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  