---
title: "setFetchDirection-Methode (SQLServerResultSet)"
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
  - SQLServerResultSet.setFetchDirection
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4ee82290-508d-4bff-a5c5-8a56338deef8
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
# setFetchDirection-Methode (SQLServerResultSet)
  Gibt Aufschluss über die Richtung, in der die Zeilen in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt verarbeitet werden.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt. Bei Verwendung dieser Methode wird die Einstellung vom JDBC\-Treiber zwar gespeichert, sie wird jedoch derzeit nicht genutzt.  
  
## Syntax  
  
```  
  
public void setFetchDirection(int direction)  
```  
  
#### Parameter  
 *direction*  
  
 Ein Wert vom Typ **int** zum Angeben der vorgeschlagenen Abrufrichtung. Folgende Werte sind möglich:  
  
 ResultSet.FETCH\_FORWARD  
  
 ResultSet.FETCH\_REVERSE  
  
 ResultSet.FETCH\_UNKNOWN  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setFetchDirection\-Methode wird von der setFetchDirection\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Der Anfangswert dieser Methode wird vom [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt bestimmt, von dem dieses SQLServerResultSet\-Objekt erstellt wurde. Die Abrufrichtung kann jedoch jederzeit geändert werden.  
  
> [!NOTE]  
>  Handelt es sich beim Cursortyp um einen Vorwärtscursor, hat die Verwendung dieser Methode keine Auswirkungen.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  