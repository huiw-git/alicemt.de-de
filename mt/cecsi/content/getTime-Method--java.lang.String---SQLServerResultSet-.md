---
title: "getTime-Methode (java.lang.String) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getTime (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e0efc0b3-4da4-45fc-9e8d-5edd9da7a42d
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
# getTime-Methode (java.lang.String) (ISQLServerResultSet)
    
## getTime\-Methode \(java.lang.String\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Time\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Time getTime(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein Time\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTime\-Methode wird von der getTime\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird ein gültiger Zeitteil eines datetime\- oder smalldatetime\-Datentyps von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben. Der Datumsteil ist dabei auf das Java\-Grunddatum \(01.01.1970\) festgelegt.  
  
## Siehe auch  
 [getTime-Methode &#40;ISQLServerResultSet&#41;](../content/getTime-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  