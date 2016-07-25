---
title: "getObject-Methode (int)"
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
  - SQLServerCallableStatement.getObject (jnt)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c4b8366b-c065-48e1-b712-19e2d9834228
caps.latest.revision: 13
caps.handback.revision: 12
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
# getObject-Methode (int)
    
## getObject\-Methode \(int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.lang.Object getObject(int index)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein **Object** \-Wert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getObject\-Methode wird von der getObject\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Von dieser Methode wird der Wert der angegebenen Spalte als Java\-Objekt zurückgegeben. Beim Typ des Java\-Objekts handelt es sich um den standardmäßigen Java\-Objekttyp, der dem SQL\-Typ der Spalte entspricht. Die Grundlage hierfür bildet die in der JDBC\-Spezifikation angegebene Zuordnung für integrierte Typen. Bei einem SQL\-NULL\-Wert wird vom Treiber ein Java\-NULL\-Wert zurückgegeben.  
  
 Diese Methode kann auch zum Lesen datenbankspezifischer, abstrakter Datentypen verwendet werden. In JDBC 2.0 wurde das Verhalten der getObject\-Methode erweitert, um Daten von benutzerdefinierten SQL\-Typen zu materialisieren. Enthält eine Spalte einen strukturierten oder unterschiedlichen Wert, entspricht das Verhalten dieser Methode einem Aufruf von `getObject(columnIndex, this.getStatement().getConnection().getTypeMap())`.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird folgendermaßen verfahren:  
  
-   Ein **date**\-Wert wird als java.sql.Date\-Objekt zurückgegeben.  
  
-   Ein **time**\-Wert wird als java.sql.Time\-Objekt zurückgegeben.  
  
-   Ein **datetime2**\-Wert wird als java.sql.Timestamp\-Objekt zurückgegeben.  
  
-   Ein **datetimeoffset**\-Wert wird als microsoft.sql.DateTimeOffset\-Objekt zurückgegeben.  
  
## Siehe auch  
 [getObject-Methode &#40;SQLServerCallableStatement&#41;](../content/getObject-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  