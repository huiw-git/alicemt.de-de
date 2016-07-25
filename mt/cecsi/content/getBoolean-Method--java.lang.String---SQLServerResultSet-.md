---
title: "getBoolean-Methode (java.lang.String) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getBoolean (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ba98a27b-722d-4904-ac65-0f082fde1fe6
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
# getBoolean-Methode (java.lang.String) (ISQLServerResultSet)
    
## getBoolean\-Methode \(java.lang.String\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **boolean** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public boolean getBoolean(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein Wert vom Typ **boolean** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBoolean\-Methode wird von der getBoolean\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Zahlen\- und Zeichendatentypen unterstützt. Von der Methode werden die Werte "1", 1 und "**true**" in **true**, die Werte "0", 0 und "**false**" in **false** konvertiert. Für alle anderen Werte bleibt das Verhalten nicht definiert.  
  
## Siehe auch  
 [getBoolean-Methode &#40;ISQLServerResultSet&#41;](../content/getBoolean-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  