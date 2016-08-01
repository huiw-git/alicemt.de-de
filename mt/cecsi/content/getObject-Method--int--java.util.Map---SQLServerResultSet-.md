---
title: "getObject-Methode (int, java.util.Map) (SQLServerResultSet)"
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
  - SQLServerResultSet.getObject (int, java.util.Map)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: df85a514-ab43-4bf6-98dd-f7f37fad1850
caps.latest.revision: 15
caps.handback.revision: 14
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
# getObject-Methode (int, java.util.Map) (SQLServerResultSet)
  Ruft unter Verwendung des Map\-Objekts den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Objekt in der Programmiersprache Java ab.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt. Bei Verwendung dieser Methode wird immer die Standardzuordnung zurückgegeben.  
  
## Syntax  
  
```  
  
public java.lang.Object getObject(int i,  
                                  java.util.Map map)  
```  
  
#### Parameter  
 *i*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *map*  
  
 Ein Map\-Objekt.  
  
## Rückgabewert  
 Ein **Object**\-Wert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getObject\-Methode wird von der getObject\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird der Wert der angegebenen Spalte als Java\-Objekt zurückgegeben. Beim Typ des Java\-Objekts handelt es sich um den standardmäßigen Java\-Objekttyp, der dem SQL\-Typ der Spalte entspricht. Die Grundlage hierfür bildet die in der JDBC\-Spezifikation angegebene Zuordnung für integrierte Typen. Bei einem SQL\-NULL\-Wert wird vom Treiber ein Java\-NULL\-Wert zurückgegeben.  
  
 Diese Methode kann auch zum Lesen datenbankspezifischer, abstrakter Datentypen verwendet werden. In der JDBC 2.0\-API wird das Verhalten der getObject\-Methode erweitert, um Daten von benutzerdefinierten SQL\-Typen zu materialisieren. Enthält eine Spalte einen strukturierten oder unterschiedlichen Wert, entspricht das Verhalten dieser Methode einem Aufruf von `getObject(columnIndex, this.getStatement().getConnection().getTypeMap())`.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird folgendermaßen verfahren:  
  
-   Ein Date\-Wert wird als java.sql.Date\-Objekt zurückgegeben.  
  
-   Ein Time\-Wert wird als java.sql.Time\-Objekt zurückgegeben.  
  
-   Ein Datetime2\-Wert wird als java.sql.Timestamp\-Objekt zurückgegeben.  
  
-   Ein Datetimeoffset\-Wert wird als microsoft.sql.DateTimeOffset\-Objekt zurückgegeben.  
  
## Siehe auch  
 [getObject-Methode &#40;ISQLServerResultSet&#41;](../content/getObject-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  