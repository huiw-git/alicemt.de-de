---
title: "getTime-Methode (java.lang.String, java.util.Calendar) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getTime (java.lang.String, java.util.Calendar)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 13b51f77-cec9-45fc-862e-3d2bb2d718d7
caps.latest.revision: 10
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
# getTime-Methode (java.lang.String, java.util.Calendar) (ISQLServerResultSet)
    
## getTime\-Methode \(java.lang.String, java.util.Calendar\) \(ISQLServerResultSet\)  
 Ruft unter Verwendung des Calendar\-Objekts den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Time\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Time getTime(java.lang.String colName,  
                             java.util.Calendar cal)  
```  
  
#### Parameter  
 *colName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *cal*  
  
 Ein Calendar\-Objekt.  
  
## Rückgabewert  
 Ein Time\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTime\-Methode wird von der getTime\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird ein gültiger Uhrzeitteil eines [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-datetime\- oder smalldatetime\-Datentyps zurückgegeben. Der Datumsteil ist dabei in der im Kalender angegebenen Zeitzone auf die Java\-Datumsbasis 01.01.1970 festgelegt.  
  
## Siehe auch  
 [getTime-Methode &#40;ISQLServerResultSet&#41;](../content/getTime-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  