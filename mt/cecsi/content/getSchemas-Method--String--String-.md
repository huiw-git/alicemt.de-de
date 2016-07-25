---
title: "getSchemas-Methode (String, String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 672171ac-976f-4605-9bee-2a5e141d92cb
caps.latest.revision: 17
caps.handback.revision: 16
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
# getSchemas-Methode (String, String)
  Ruft die in der aktuellen Datenbank verfügbaren Schemanamen unter Verwendung des angegebenen Katalognamens und des Schemanamens ab.  
  
## Syntax  
  
```  
  
public ResultSet getSchemas(java.lang.String catalog,  
                       java.lang.String schemaPattern)  
```  
  
#### Parameter  
 *catalog*  
  
 Der Name eines Katalogs in der Datenbank. Bei einer leeren Zeichenfolge \(""\) enthält das Ergebnis die Schemas ohne einen Katalog. Bei **null** wird der Katalogname nicht für die Suche verwendet.  
  
 *schemaPattern*  
  
 Der Name eines Schemas. Bei **null** wird der Schemaname nicht für die Suche verwendet.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSchemas\-Methode wird von der getSchemas\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getSchemas\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_SCHEM|**String**|Der Name des Schemas.|  
|TABLE\_CATALOG|**String**|Der Katalogname für das Schema.|  
  
 Die Ergebnisse werden nach "TABLE\_CATALOG" und anschließend nach "TABLE\_SCHEM" sortiert. In jeder Zeile bildet "TABLE\_SCHEM" die erste Spalte und "TABLE\_CATALOG" die zweite Spalte.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  