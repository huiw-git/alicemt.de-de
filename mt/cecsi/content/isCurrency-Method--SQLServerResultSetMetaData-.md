---
title: "isCurrency-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.isCurrency
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7fe25d90-693c-4d3b-9dd2-0f8351c5a9ed
caps.latest.revision: 7
caps.handback.revision: 7
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
# isCurrency-Methode (SQLServerResultSetMetaData)
    
## isCurrency\-Methode \(SQLServerResultSetMetaData\)  
 Gibt an, ob es sich bei der angegebenen Spalte um einen Währungswert handelt.  
  
## Syntax  
  
```  
  
public boolean isCurrency(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 **true**, wenn die Spalte einen Währungswert besitzt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isCurrency\-Methode wird von der isCurrency\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
 Von dieser Methode wird **true** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nur mit money\- und smallmoney\-Datentypen zurückgegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  