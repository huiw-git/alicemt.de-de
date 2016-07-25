---
title: "getDate-Methode (int, java.util.Calendar) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getDate (int, java.util.Calendar)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 150411f7-2a73-4380-b921-9698acd5d1f9
caps.latest.revision: 11
caps.handback.revision: 10
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
# getDate-Methode (int, java.util.Calendar) (ISQLServerResultSet)
    
## getDate\-Methode \(int, java.util.Calendar\) \(ISQLServerResultSet\)  
 Ruft unter Verwendung des Calendar\-Objekts den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Date\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Date getDate(int columnIndex,  
                             java.util.Calendar cal)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *cal*  
  
 Ein Calendar\-Objekt.  
  
## Rückgabewert  
 Ein Date\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getDate\-Methode wird von der getDate\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird ein gültiger Datumsteil eines [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-datetime\- oder smalldatetime\-Datentyps zurückgegeben. Der Zeitteil ist dabei in der im Kalender angegebenen Zeitzone auf die Java\-Zeitbasis 00:00 \(Mitternacht\) festgelegt.  
  
## Siehe auch  
 [getDate-Methode &#40;ISQLServerResultSet&#41;](../content/getDate-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  