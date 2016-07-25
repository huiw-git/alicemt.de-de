---
title: "executeUpdate-Methode (java.lang.String, java.lang.String)"
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
  - SQLServerStatement.executeUpdate (java.lang.String[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2f44a689-65c8-4c94-9574-e9c08ea7918e
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
# executeUpdate-Methode (java.lang.String, java.lang.String)
  Führt die angegebene SQL\-Anweisung aus und signalisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], dass die automatisch generierten Schlüssel, die in dem angegebenen Array angegeben sind, zum Abrufen verfügbar gemacht werden sollen.  
  
## Syntax  
  
```  
  
public final int executeUpdate(java.lang.String sql,  
                               java.lang.String[] columnNames)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *columnNames*  
  
 Ein Array vom Typ **String**, mit dem angegeben wird, welche Spaltennamen der automatisch generierten Schlüssel verfügbar gemacht werden sollen.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der betroffenen Zeilen \("0" bei Verwendung einer DDL\-Anweisung\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese executeUpdate\-Methode wird von der executeUpdate\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Wenn beim Ausführen einer gespeicherten Prozedur eine Updatezählung größer als 1 erhalten oder mehrere Resultsets generiert werden, führen Sie die gespeicherte Prozedur mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode aus.  
  
## Siehe auch  
 [executeUpdate-Methode &#40;SQLServerStatement&#41;](../content/executeUpdate-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  