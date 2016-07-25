---
title: "getString-Methode (int) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getString (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bfa493c4-fe07-449b-b4d0-384e1a1fce48
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
# getString-Methode (int) (ISQLServerResultSet)
    
## getString\-Methode \(int\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **String** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.lang.String getString(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **String** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getString\-Methode wird von der getString\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Alle Spalten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] können als Zeichenfolge zurückgegeben werden. Es können also die **String** \-Darstellung aller zahlen\- und zeichenfolgenbasierten Typen und eine hexadezimale Zeichenfolgendarstellung binärer Spalten wie "binary", "varbinary", "varbinary\(max\)", "image", "timestamp" oder "uniqueidentifier" zurückgegeben werden.  
  
 Den Speicherort berücksichtigende Typen wie "money", "smallmoney", "datetime", "smalldatetime", "float", "real", "decimal" oder "numeric" geben für den zugrundeliegenden Wert des Typs das kanonische toString\(\)\-Format zurück.  
  
 Benutzerdefinierte Typen werden als hexadezimale **String** \-Werte zurückgegeben.  
  
## Siehe auch  
 [getString-Methode &#40;ISQLServerResultSet&#41;](../content/getString-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  