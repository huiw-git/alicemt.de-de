---
title: "getTimestamp-Methode (int) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getTimestamp (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ad538a76-983f-4175-9481-9e7fa9480c71
caps.latest.revision: 8
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
# getTimestamp-Methode (int) (ISQLServerResultSet)
    
## getTimestamp\-Methode \(int\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltenindex in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Timestamp\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Timestamp getTimestamp(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein Timestamp\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTimestamp\-Methode wird von der getTimestamp\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden nur Werte aus datetime\- und smalldatetime\-Spalten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben.  
  
## Siehe auch  
 [getTimestamp-Methode &#40;ISQLServerResultSet&#41;](../content/getTimestamp-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  