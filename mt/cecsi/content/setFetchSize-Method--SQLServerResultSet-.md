---
title: "setFetchSize-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.setFetchSize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 233bf4f8-4758-42d0-a80b-33e34fa78027
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
# setFetchSize-Methode (ISQLServerResultSet)
    
## setFetchSize\-Methode \(ISQLServerResultSet\)  
 Gibt für den JDBC\-Treiber an, wie viele Zeilen aus der Datenbank abgerufen werden sollen, wenn für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt weitere Zeilen benötigt werden.  
  
## Syntax  
  
```  
  
public void setFetchSize(int rows)  
```  
  
#### Parameter  
 *rows*  
  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der abzurufenden Zeilen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setFetchSize\-Methode wird von der setFetchSize\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Ist die angegebene Abrufgröße NULL, wird der Wert vom JDBC\-Treiber ignoriert und die korrekte Abrufgröße geschätzt. Der Standardwert wird von dem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt festgelegt, von dem das Resultset erstellt wurde. Die Abrufgröße kann jedoch jederzeit geändert werden.  
  
 Mit dieser Methode wird die Blockabrufgröße für Servercursor geändert. Die Änderungen treten beim nächsten Aufruf von "sp\_cursorfetch" durch den JDB\-Treiber in Kraft. Durch das Festlegen der Abrufgröße auf NULL wird die Standardabrufgröße für den momentan verwendeten Cursortyp wiederhergestellt.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  